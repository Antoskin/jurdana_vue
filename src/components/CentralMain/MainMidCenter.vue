<template>
            <div class="middle-centr">
                        <div class="middle-center-top">
                            <p>ATTORNEYS’ ASSOCIATION</p>
                        </div>
                        <div class="middle-center-mid">
                            <i class="fas fa-chevron-left"></i>
                            <h1 class="h1-target">
                                We assist in decision-making solving complicated legal issues
                            </h1>
                            <i class="fas fa-chevron-right"></i>
                        </div>
                        <div class="middle-center-bot">
                            <img class="btn-next" height="30" src="../../assets/mouse.svg" alt="">
                        </div>
            </div>
</template>


<script>
    export default {
        name: 'MainMidCenter'
    }
</script>

<style>
    h1 {
            font-size: 40px;
            line-height: 40px;
            max-width: 610px;
            margin: 0 auto;
    }
    .middle-centr {
        width: 100%;
        display: flex;
        flex-direction: column;
    }

    .middle-centr .middle-center-top {
        height: 30px;
        text-align: center;
    }

    .middle-centr .middle-center-top p {
        letter-spacing: 3px;
    }

    .middle-centr .middle-center-mid {
        height: 90%;
        text-align: center;
        display: flex;
        align-items: center;
        position: relative;
    }

    .middle-centr .middle-center-mid h1 {
        text-align: center;
    }

    .middle-centr .middle-center-mid i {
        position: absolute;
        top: 0;
        bottom: 0;
        margin: auto;
        cursor: pointer;
        display: none;
    }

    .middle-centr .middle-center-mid .fa-chevron-left {
        left: 10px;
    }

    .middle-centr .middle-center-mid .fa-chevron-right {
        right: 10px;
    }

    .middle-centr .middle-center-bot {
        height: 30px;
        text-align: center;
    }

    .middle-centr .middle-center-bot .btn-next {
        //animation: topDown 1s infinite ease-in-out;
    }
</style>