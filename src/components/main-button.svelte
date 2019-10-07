<script>
    import { fly } from 'svelte/transition';
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();

    export let modifier = "";
    export let socialMod = "";
    export let duration = 0;
    export let transValue = 0;
    export let action = "";

    function handleClick () {
        dispatch('click', {
            action: action
        });
    }
</script>

<style>
    .chat-button {
        display: block;
        width: 66px;
        height: 66px;
        background-color: #76dff4;
        background-image: url('img/phone.png');
        background-repeat: no-repeat;
        background-position: center;
        border: none;
        border-radius: 50%;
        cursor: pointer;
    }

    .chat-button:hover,
    .chat-button:focus {
        background-color: #adecf8;
    }

    .chat-button--slave {
        margin-right: 15px;
        width: 45px;
        height: 45px;
        background-color: #adecf8;
    }

    .chat-button--slave:hover,
    .chat-button--slave:focus {
        background-color: #76dff4;
    }
    
    .chat-button--email {
        background-image: url('img/email.png');
    }

    .chat-button--chat {
        background-image: url('img/chat.png');
    }

    .chat-button--fb {
        background-image: url('img/facebook.png');
    }

    .chat-button--vk {
        background-image: url('img/vk.png');
    }

    .chat-button--tg {
        background-image: url('img/telegram.png');
    }
</style>

<button 
class="chat-button {modifier} {socialMod}" 
transition:fly="{ {x: transValue, duration: duration} }"
on:mouseover
on:mouseout
on:click={ handleClick }
>
</button>