<script>
    export let addClasses = '';
    export let inPanel = false;
</script>

<style>
    .cross-button {
        position: relative;
        width: 25px;
        height: 25px;
        background-color: #f1f2f2;
        border: 1px solid #1e1d1f;
        border-radius: 50%;
        cursor: pointer;
    }

    .cross-button::before,
    .cross-button::after {
        content: '';
        position: absolute;
        display: block;
        top: calc(50% - 1px/2);
        left: calc(50% - 10px/2);
        width: 10px;
        height: 1px;
        background-color: #1e1d1f;
        transform-origin: 50%;
    }

    .cross-button::before {
        transform: rotate(45deg);
    }

    .cross-button::after {
        transform: rotate(-45deg);
    }
    
    .cross-button--in-panel {
        position: absolute;
        left: -33px;
        top: 0;
    }
</style>

<button 
class="cross-button {addClasses}" 
class:cross-button--in-panel={inPanel} 
on:click
>
</button>