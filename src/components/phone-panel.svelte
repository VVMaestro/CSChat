<script>
    import CrossButton from './cross-button.svelte';
</script>

<style>
    .phone-panel__box {
        position: fixed;
        right: 15px;
        bottom: 180px;
        box-sizing: border-box;
        padding-top: 40px;
        padding-left: 77px;
        width: 550px;
        height: 150px;
        font-family: 'Oswald', Arial, Helvetica, sans-serif;
        background-color: #ff9400;
        background-color: var(--orange);
        background-image: url('img/backlay.png');
        background-repeat: no-repeat;
        background-size: cover;
        border-radius: 12px;
        box-shadow: 0 0 10px 4px #d3d3d3;
    }

    .phone-panel__logo {
        position: absolute;
        top: 10px;
        right: 10px;
        width: 48px;
        height: auto;
    }

    .phone-panel__title {
        margin: 0 0 10px 0;
        font-size: 21px;
        font-weight: 400;
    }

    .phone-pannel__phone {
        box-sizing: border-box;
        padding-left: 25px;
        width: 300px;
        height: 50px;
        font-family: inherit;
        font-weight: 400;
        font-size: 20px;
        border-radius: 8px;
        border: 1px solid #e1e4e8;
    }

    .phone-pannel__phone::-webkit-input-placeholder {
        color: #dfdfdf;
    }

    .phone-pannel__phone:-ms-input-placeholder {
        color: #dfdfdf;
    }

    .phone-pannel__phone::-ms-input-placeholder {
        color: #dfdfdf;
    }

    .phone-pannel__phone:-moz-placeholder {
        color: #dfdfdf;
    }

    .phone-pannel__phone::-moz-placeholder {
        color: #dfdfdf;
    }

    .phone-pannel__phone::placeholder {
        color: #dfdfdf;
    }

    .phone-panel__submit {
        width: 145px;
        height: 50px;
        font-family: 'Oswald', Arial, Helvetica, sans-serif;
        color: #fff;
        font-size: 20px;
        background-color: #76dff4;
        border-radius: 8px;
        border: none;
        cursor: pointer;
    }

    .phone-panel__submit:hover,
    .phone-panel__submit:focus {
        background-color: #adecf8;
    }

    .phone-panel__policy {
        position: absolute;
        display: inline-block;
        right: 48px;
        bottom: 100%;
        padding: 0 15px;
        height: 18px;
        color: #1c1d1e;
        font-size: 10px;
        font-weight: 100;
        text-decoration: none;
        vertical-align: middle;
        line-height: 18px;
        background-color: #eaeaea;
        border-top-right-radius: 7px;
        border-top-left-radius: 7px;
        box-shadow: 0 -5px 10px -5px #d3d3d3,
                    10px 0 10px -5px #d3d3d3,
                    -10px 0 10px -5px #d3d3d3;
    }
</style>

<div class="phone-panel__box" >
    <CrossButton inPanel={true} on:click />
    <img class="phone-panel__logo" src="img/degame.png" alt="Логотип">
    <form>
        <h3 class="phone-panel__title">Оставьте номер и мы перезвоним вам</h3>
        <div class="phone-pannel__wrapper">
            <input class="phone-pannel__phone" type="tel" placeholder="Номер телефона">
            <input class="phone-panel__submit" type="submit">
        </div>
    </form>
    <a href="#" class="phone-panel__policy">Политика конфиденциальности</a>
</div>