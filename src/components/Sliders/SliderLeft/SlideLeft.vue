<template>
        <div class="left-side">
            <video class="back-video"  id="bgvid" playsinline autoplay muted loop>
                <source src="../../../assets/bback.mp4" type="video/mp4">
            </video>
            <div class="left-slider">
                <SlideLeftTop></SlideLeftTop>
                <SlideLeftMiddle></SlideLeftMiddle>
                <div class="left-slide-bot"></div>
                <span class="action-left">OUR SERVICES</span>
            </div>
        </div>
</template>



<script>
    import SlideLeftTop from './SlideLeftTop'
    import SlideLeftMiddle from './SlideLeftMiddle'

    export default {
        name: 'SlideLeft',
        components: {
            SlideLeftTop,
            SlideLeftMiddle
        }
    }
</script>

<style scoped>
   .left-side {
        width: 50%;
        height: 100%;
        border-right: 1px solid #4b536c;
        // overflow: hidden;
        //background: #5067b0f5;
        position: relative;  
    }
      .left-slider {
            width: 100%;
            background: #5067b0f5;
            height:60%;
            position: absolute;
            top: 0;
            bottom: 0;
            margin: auto;
            z-index: 100;
            display: flex;
            flex-direction: column;
            background:rgba(80, 103, 176, 0.96);
            left:-95%;
        }
              .left-slide-bot {
                height: 150px;
                background: url('../../../assets/dotted.svg');
                background-position: center;
                height: 90px;
                margin: 30px 30px ;
                // opacity: 0;
            }
                .action-left {
                    text-align: center;
                    line-height: 38px;
                    display: none;
                    letter-spacing: 2px;
                }

             
</style>