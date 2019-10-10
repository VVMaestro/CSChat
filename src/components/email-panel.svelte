<script>
    import CrossButton from './cross-button.svelte';
    import PanelHeader from './panel-header.svelte';
</script>

<style>
    .email-panel__box {
        position: fixed;
        right: 15px;
        bottom: 180px;
        width: 375px;
        height: 450px;
        font-family: 'Oswald', Arial, Helvetica, sans-serif;
        border-radius: 12px;
        box-shadow: 0 0 10px 4px #d3d3d3;
        background-color: #f3f5f7;
    }

    .email-panel__body {
        box-sizing: border-box;
        padding: 25px 15px 35px;
        height: calc(450px - 60px);
    }

    .email-panel__form {
        display: flex;
        justify-content: flex-start;
        flex-direction: column;
        height: 100%;
    }

    .email-panel__input {
        box-sizing: border-box;
        margin-bottom: 15px;
        padding: 0 20px;
        width: 100%;
        height: 45px;
        font-family: 'Oswald', Arial, Helvetica, sans-serif;
        font-size: 15px;
        border: 1px solid #e1e4e8;
        border-radius: 4px;
    }

    .email-panel__input::-webkit-input-placeholder {
        color: #ccccff;
    }

    .email-panel__input:-ms-input-placeholder {
        color: #ccccff;
    }

    .email-panel__input::-ms-input-placeholder {
        color: #ccccff;
    }

    .email-panel__input:-moz-placeholder {
        color: #ccccff;
    }

    .email-panel__input::-moz-placeholder {
        color: #ccccff;
    }

    .email-panel__input::placeholder {
        color: #ccccff;
    }

    .email-panel__text {
        box-sizing: border-box;
        width: 100%;
        padding: 15px 20px 0 20px;
        height: 130px;
        font-family: 'Oswald', Arial, Helvetica, sans-serif;
        font-size: 15px;
        border: 1px solid #e1e4e8;
        border-radius: 4px;
        resize: none;
    }

    .email-panel__text::-webkit-input-placeholder {
        color: #ccccff;
    }

    .email-panel__text:-ms-input-placeholder {
        color: #ccccff;
    }

    .email-panel__text::-ms-input-placeholder {
        color: #ccccff;
    }

    .email-panel__text:-moz-placeholder {
        color: #ccccff;
    }

    .email-panel__text::-moz-placeholder {
        color: #ccccff;
    }

    .email-panel__text::placeholder {
        color: #ccccff;
    }

    .email-panel__submit {
        margin-top: auto;
        width: 100%;
        height: 40px;
        font-family: 'Oswald', Arial, Helvetica, sans-serif;
        color: #fff;
        font-size: 17px;
        border-radius: 4px;
        border: 1px solid #e1e4e8;
        background-color: #ccccff;
        cursor: pointer;
    }
</style>

<div class="email-panel__box">
    <CrossButton inPanel={true} on:click />
    <PanelHeader />
    <section class="email-panel__body">
        <form class="email-panel__form">
            <input type="text" class="email-panel__input" placeholder="Ваше имя">
            <input type="email" class="email-panel__input" placeholder="Ваш email">
            <textarea class="email-panel__text" placeholder="Ваше сообщение"></textarea>
            <input type="submit" class="email-panel__submit" value="Отправить">
        </form>
    </section>
</div>