<template>
        <div class="right-side">
            <div class=" right-slider">
                <RightSlideTop></RightSlideTop>
                <RightSlideMiddle></RightSlideMiddle>
                <div class="right-slide-bot"></div>
                <span class="action-right">CONTACT US</span>
            </div>
        </div>
</template>



<script>

    import RightSlideTop from './SlideRightTop.vue'
    import RightSlideMiddle from './SlideRightMiddle.vue'

    import { TweenLite } from 'gsap'

    import {bus} from '../../../main.js'



    export default {
        name: 'SlideRight',
        components: {
            RightSlideTop,
            RightSlideMiddle
        },
        created() {
            bus.$on(`slideOpenR`, () => {
                openRightSlide()
            })
        }
    }


    const openRightSlide = () => {
        let tl = TweenLite
        tl.to(`.right-slider`, .5, {'right': 0})
        tl.fromTo(`.r-s-close img`, .5, {'margin': 0}, { 'margin': '20px 0' }).delay(2)
        tl.fromTo(`.r-s-close span`, 5, {'opacity': 0}, { 'opacity': 1 }).delay(2.5)
        tl.to(`.right-slider`, .5, {'height': '100%'}).delay(.7)
        tl.fromTo(`.right-slide-mid, .right-slide-top, .right-slide-bot`, .5, { opacity:0, 'visibility':'hidden' }, { opacity: 1, 'visibility':'visible' },.5  ).delay(1.5)
    }
</script>


<style scoped>

    .right-side {
        width: 50%;
        height: 100%;
        border-right: 1px solid #4b536c;
        overflow: hidden;
        background: #212b4a;
        position: relative;
    }
    .right-slider {
            width: 100%;
            height: 60%;
            background:#383938; 
            position: absolute;
            top: 0;
            bottom: 0;
            margin: auto;
            z-index: 100;
            display: flex;
            flex-direction: column;
            right:-95%;
    }

    .right-slide-bot {
            height: 150px;
            background: url('../../../assets/dotted.svg');
            background-position: center;
            height: 90px;
            margin: 30px 30px ;
            //opacity: 0;
    }
       
            .action-right {
                    text-align: center;
                    line-height: 38px;
                    display: none;
                    letter-spacing: 2px;
            }
</style>