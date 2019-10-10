<script>
    import CrossButton from './cross-button.svelte';
    import PanelHeader from './panel-header.svelte';
</script>

<style>
    .chat-panel__box {
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

    .chat-panel__scroll-wrapper {
        height: 330px;
        overflow-y: scroll;
    }

    .chat-panel__body {
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        flex-grow: 1;
        box-sizing: border-box;
        padding: 35px 15px;
    }

    .chat-panel__message {
        max-width: 70%;
        margin: 7px 0;
        padding: 5px;
        font-size: 13px;
        color: #1e1c1d;
        border: 1px solid #cad8e6;
        border-radius: 4px;
    }

    .chat-panel__message--outgo {
        align-self: flex-end;
        background-color: #d4e7fa;
    }

    .chat-panel__message--ingo {
        align-self: flex-start;
        background-color: #fff;
    }

    .chat-panel__send-wrapper {
        box-sizing: border-box;
        padding-right: 15px;
        width: 100%;
        height: 60px;
        border-top: 1px solid #cad8e6;
        border-bottom-left-radius: 12px;
        border-bottom-right-radius: 12px;
        background-color: #fff;
    }

    .chat-panel__send-wrapper form {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .chat-panel__textarea {
        box-sizing: border-box;
        padding: 15px 0 15px 25px;
        width: 84%;
        height: 59px;
        font-family: 'Oswald', Arial, Helvetica, sans-serif;
        font-size: 17px;
        color: #ccccff;
        border: none;
        outline: none;
        border-bottom-left-radius: 12px;
        resize: none;
    }

    .chat-panel__textarea::-webkit-input-placeholder {
        color: #ccccff;
    }

    .chat-panel__textarea:-ms-input-placeholder {
        color: #ccccff;
    }

    .chat-panel__textarea::-ms-input-placeholder {
        color: #ccccff;
    }

    .chat-panel__textarea:-moz-placeholder {
        color: #ccccff;
    }

    .chat-panel__textarea::-moz-placeholder {
        color: #ccccff;
    }

    .chat-panel__textarea::placeholder {
        color: #ccccff;
    }

    .chat-panel__send-button {
        width: 35px;
        height: 28px;
        border: none;
        background-image: url('img/send.png');
        background-position: center;
        background-repeat: no-repeat;
        background-color: transparent;
        cursor: pointer;
    }
</style>

<div class="chat-panel__box">
    <CrossButton inPanel={true} on:click />
    <PanelHeader />
    <div class="chat-panel__scroll-wrapper">
        <section class="chat-panel__body">
            <span class="chat-panel__message chat-panel__message--outgo">
                Здравствуйте
            </span>
            <span class="chat-panel__message chat-panel__message--outgo">
                Мы бы очень сильно хотели заказать у вас сайт но сомневаемся в выборе. Вы не могли бы помочь? 
                Нужен продающий сайт для одного товара, но с хорошим SEO
            </span>
            <span class="chat-panel__message chat-panel__message--ingo">
                Здравствуйте
            </span>
            <span class="chat-panel__message chat-panel__message--ingo">
                Как менеджер прочитает сообщение, он тут же ответит.
            </span>
            <span class="chat-panel__message chat-panel__message--ingo">
                Как менеджер прочитает сообщение, он тут же ответит.
            </span><span class="chat-panel__message chat-panel__message--ingo">
                Как менеджер прочитает сообщение, он тут же ответит.
            </span><span class="chat-panel__message chat-panel__message--ingo">
                Как менеджер прочитает сообщение, он тут же ответит.
            </span><span class="chat-panel__message chat-panel__message--ingo">
                Как менеджер прочитает сообщение, он тут же ответит.
            </span><span class="chat-panel__message chat-panel__message--ingo">
                Как менеджер прочитает сообщение, он тут же ответит.
            </span>
        </section>
    </div>
    <section class="chat-panel__send-wrapper">
        <form>
            <textarea name="" id="" class="chat-panel__textarea" placeholder="Введите сообщение"></textarea>
            <input type="submit" class="chat-panel__send-button" value="">
        </form>
    </section>
</div>