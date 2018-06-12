<template>
       <div class="left-slide-top">
                    <div class="slide-dots-back"></div>
                    <div class="l-s-close">
                        <img class="m-c" width="15" src="@/assets/arow 1.svg" alt="">
                        <span class="m-c">CLOSE</span>
                        <img class="m-c" width="15" src="@/assets/arow 2.svg" alt="">
                        <img class="m-o" src="@/assets/m-close.png" alt="">
                    </div>
        </div>
</template>

<script>
    
    export default {
        name: 'SlideLeftTop'
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