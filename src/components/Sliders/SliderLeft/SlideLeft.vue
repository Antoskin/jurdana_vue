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

    import { TweenLite } from 'gsap'

    import { bus } from '../../../main.js'


    export default {
        name: 'SlideLeft',
        components: {
            SlideLeftTop,
            SlideLeftMiddle
        },
        created() {
            bus.$on('slideOpenL', () => {
                openLeftSlide()
            })
        }

    }

    const openLeftSlide = () => {
        TweenLite.to(`.left-slider`, .5, {'left': 0})
        TweenLite.fromTo(`.l-s-close img`, .5, {'margin': 0}, { 'margin': '20px 0' }).delay(2)
        TweenLite.fromTo(`.l-s-close span`, 5, {'opacity': 0}, { 'opacity': 1 }).delay(2.5)
        TweenLite.to(`.left-slider`, .5, {'height': '100%'}).delay(.7)
        TweenLite.fromTo(`.left-slide-mid, .left-slide-top, .left-slide-bot`, .5, { opacity:0, 'visibility':'hidden' }, { opacity: 1, 'visibility':'visible' },.5  ).delay(1.5)
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