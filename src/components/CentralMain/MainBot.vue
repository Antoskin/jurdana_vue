<template>
        <div class="bottom-line">
                    <div class="bottom-left">
                        <p class="copir-t">All rights reserved © Jurdana, 2018</p>
                    </div>
                    <div class="bottom-middle">
                        <a href="tel:+380445748490">
                            <i class="fas fa-mobile-alt"></i> +38 (044) 574-84-90
                        </a>
                        <a class="email" href="mailto:info@jurdana.com.ua">
                            <i class="fas fa-envelope"></i> info@jurdana.com.ua
                        </a>
                        <a class="location"href="#">
                            <i class="fas fa-compass"></i> 22 Sribnokilska, Str.Kyiv 02095, Ukraine
                        </a>
                    </div>
                    <div class="bottom-right">
                        <a href="http://www.opex.company/" target="_blank">
                            <img width="125" src="../../assets/opex logo.svg" alt="">
                        </a>
                    </div>
        </div>
</template>

<script>
    export default {
        name: 'MainBot'
    }
</script>


<style scoped>
    .bottom-line {
        height: 44px;
        display: flex;
        justify-content: space-between;
        color: #BCBFC8;;
    }

    .bottom-left {
        display: flex;
        align-items: center;
    }

    .bottom-middle {
        display: flex;
        align-items: center;
    }

    .bottom-middle .email {
        margin: 0 10px;
    }

    .bottom-middle a {
        font-size: 15px;
        transition: .5s ease-in-out;
        color: #BCBFC8;
    }

    .bottom-middle a i {
        padding-right: 3px;
        color: #fff;
    }

    .bottom-middle a:hover {
        color: #fff;
    }

    .bottom-right {
        display: flex;
        align-items: flex-end;
        justify-content: flex-end;
    }
</style>