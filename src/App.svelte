<script>
	import Global from './components/global.svelte';
	import MainButton from './components/main-button.svelte';
	import PhonePanel from './components/phone-panel.svelte';

	let visible = false;
	let buttonsOutTimeout;
	let isShow = {
		phone : false,
		email : false,
		chat  : false
	};

	function handleMouseOut () {
		buttonsOutTimeout = setTimeout(() => {
			visible = false;
		}, 3000);
	}

	function handleMouseOver () {
		if (buttonsOutTimeout) clearTimeout(buttonsOutTimeout);
		visible = true;
	}

	function handleClick (e) {
		isShow[e.detail.action] = true;
	}

	let slaveButtons = [
		{socialMod: 'chat-button--email', duration: 100, transValue: 50, action: 'email'},
		{socialMod: 'chat-button--chat', duration: 200, transValue: 100, action: 'chat'},
		{socialMod: 'chat-button--vk', duration: 300, transValue: 150, action: 'vk'},
		{socialMod: 'chat-button--tg', duration: 400, transValue: 200, action: 'tg'},
		{socialMod: 'chat-button--fb', duration: 500, transValue: 250, action: 'fb'}
	];
</script>

<style>
	.button-pannel {
		position: fixed;
		right: 15px;
		bottom: 90px;
		display: flex;
		flex-direction: row-reverse;
		justify-content: flex-start;
		align-items: center;
	}
</style>

{#if isShow.phone}
	<PhonePanel on:click={() => { isShow.phone = false; } } />
{/if}
{#if isShow.email}
	
{/if}
<div class="button-pannel">
	<MainButton 
	on:mouseout={ handleMouseOut } 
	on:mouseover={ handleMouseOver } 
	on:click={ handleClick } 
	action={ 'phone' }
	/>
	{#if visible}
		{#each slaveButtons as slave}
			<MainButton 
			on:mouseout={ handleMouseOut } 
			on:mouseover={ handleMouseOver } 
			modifier={ 'chat-button--slave' } 
			socialMod={ slave.socialMod } 
			duration={ slave.duration } 
			transValue={ slave.transValue } 
			on:click={ handleClick } 
			action={ slave.action }
			/>
		{/each}
	{/if}
</div>