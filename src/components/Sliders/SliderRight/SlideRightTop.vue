<template>
        <div class="right-slide-top">
                    <div class="slide-dots-back"></div>
                    <div class="r-s-close">
                        <img class="m-c" width="15" src="../../../assets/arow 1.svg" alt="">
                        <span class="m-c">CLOSE</span>
                        <img class="m-c" width="15" src="../../../assets/arow 2.svg" alt="">
                        <img class="m-o" src="../../../assets/m-close.png" alt="">
                    </div>
        </div>
</template>

<script>
    export default {
        name: 'RightSlideTop'
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