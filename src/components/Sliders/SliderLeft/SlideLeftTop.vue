<template>
       <div class="left-slide-top">
                    <div class="slide-dots-back"></div>
                    <div @click="closeLeftSlide" class="l-s-close">
                        <img class="m-c" width="15" src="@/assets/arow 1.svg" alt="">
                        <span class="m-c">CLOSE</span>
                        <img class="m-c" width="15" src="@/assets/arow 2.svg" alt="">
                        <img class="m-o" src="@/assets/m-close.png" alt="">
                    </div>
        </div>
</template>

<script>
    
    export default {
        name: 'SlideLeftTop',
        methods: {
        	closeLeftSlide: () => {
				closeLeftSlide()
        	}
        }
    }

	const closeLeftSlide = () => {
	    TweenLite.fromTo(`.left-slide-mid, .left-slide-top, .left-slide-bot`, .5, { opacity:1, 'visibility':'visible' }, { opacity: 0, 'visibility':'hidden' },.5  )
	    TweenLite.to(`.left-slider`, .5, {'height': '60%'}).delay(.7)
	    TweenLite.to(`.left-slider`, .5, {'left': '-95%'}).delay(1.5)
	    TweenLite.to(`.l-s-close span`, .5, { 'opacity': 0 })
	}

</script>

<style scoped>
.left-slide-top
{
	display: flex;
	height: 90px;
	margin: 30px 30px;
	// opacity: 0;
	// visibility: hidden;
}
.slide-dots-back
{
	background: url('../../../assets/dotted.svg');
	background-position: center;
	width: 100%;
}
.l-s-close
{
	align-items: center;
	cursor: pointer;
	display: flex;
	flex-direction: column;
	justify-content: center;
	opacity: .7;
	transition: .3s ease-in-out;
	width: 60px;
}
.l-s-close:hover
{
	opacity: 1;
}
.m-c
{
	margin: 10px 0;
}
span
{
	color: #fff;
	font-size: 11px;
	letter-spacing: 2px;
	opacity: 0;
	transform: rotate(-90deg);
	width: 40px;
}
.m-o
{
	display: none;
}
</style>