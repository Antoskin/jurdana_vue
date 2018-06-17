<template>
        <div class="right-slide-top">
                    <div class="slide-dots-back"></div>
                    <div @click="closeRightSlide" class="r-s-close">
                        <img class="m-c" width="15" src="../../../assets/arow 1.svg" alt="">
                        <span class="m-c">CLOSE</span>
                        <img class="m-c" width="15" src="../../../assets/arow 2.svg" alt="">
                        <img class="m-o" src="../../../assets/m-close.png" alt="">
                    </div>
        </div>
</template>

<script>
    import {TweenLite} from 'gsap'
    export default {
        name: 'RightSlideTop',
        methods: {
            closeRightSlide: () => {
                closeRightSlide()
            }
        }
    }

    const closeRightSlide = () => {
        let tl = TweenLite
        tl.fromTo(`.right-slide-mid, .right-slide-top, .right-slide-bot`, .5, { opacity:1, 'visibility':'visible' }, { opacity: 0, 'visibility':'hidden' }, .5  )
        tl.to(`.right-slider`, .5, {'height': '60%'}).delay(.7)
        tl.to(`.right-slider`, .5, {'right': '-95%'}).delay(1.5)
        tl.to(`.r-s-close span`, .5, { 'opacity': 0 })
    }
</script>


<style scoped>

    .right-slide-top { 
                flex-direction: row-reverse; 
                height: 90px;
                margin: 30px 30px ;
                display: flex;
                //opacity: 0;
                // visibility: hidden;
    }
           .slide-dots-back {
                    width: 100%;
                    background: url('../../../assets/dotted.svg');
                    background-position: center;
            }
              .r-s-close {
                    cursor: pointer;
                    width: 60px;
                    display: flex;
                    flex-direction: column;
                    align-items: center;
                    justify-content: center;
                    opacity: .7;
                    transition: .3s ease-in-out;
                
                  
                }
                .r-s-close:hover {
                    opacity: 1;
                }
                .m-c {
                        margin: 10px 0;
                }
                span {
                        transform: rotate(-90deg);
                        width: 40px;
                        font-size: 11px;
                       color:#fff;
                        //opacity: 0;
                        letter-spacing: 2px;
                }
                .m-o {
                        display:none
                }
</style>