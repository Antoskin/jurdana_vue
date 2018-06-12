<template>
        <div class="middle-line">
            <MainMidLeft></MainMidLeft>
            <MainMidCenter></MainMidCenter>
            <MainMidRight></MainMidRight>
        </div>
</template>

<script>
    import MainMidLeft from './MainMidLeft.vue'
    import MainMidRight from './MainMidRight.vue'
    import MainMidCenter from './MainMidCenter.vue'
    export default {
        name: 'MainMid',
        components: {
            MainMidLeft,
            MainMidRight,
            MainMidCenter
        }
    }
</script>

<style scoped>
    .middle-line {
        height: 380px;
        width: 100%;
        margin: auto 0;
        display: flex;
        justify-content: space-between;
        color:#fff;
    }
</style>