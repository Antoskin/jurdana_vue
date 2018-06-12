<template>
        <div class="top-line">
                    <a href="#" class="link-logo">
                            <img width="228" src="../../assets/logo jurdana.svg" alt="">
                    </a>
                    <div class="lang-switch">
                        <a class="activ" href="#">EN</a>
                        <a href="#">UA</a>
                    </div>
        </div>
</template>

<script>
    export default {
            name: 'MainT'
    }
</script>

<style scoped>
    .top-line {
        display: flex;
        justify-content: space-between;
    }

    .lang-switch a {
        text-decoration: none;
        color: #fff;
        margin-left: 10px;
    }

    .activ {
        font-weight: bold;
    }
</style>