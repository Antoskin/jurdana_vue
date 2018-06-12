<template>
        <div class="right-slide-mid">
                    <p>FEEDBACK FORM</p>
                    <h3>Contact us</h3>
                    <form id="contact-form" action="#">
                        <input class="in-area" type="text" placeholder="Your name">
                        <input class="in-area" type="text" placeholder="Your phone number">
                        <input class="in-area" type="text" placeholder="Your @">
                        <textarea class="in-area textareas " type="text" placeholder="Your message" resize="none" ></textarea>
                        <input class="sendMsg" type="submit" value="Send">
                    </form>
        </div>
</template>

<script>
    export default {
        name: 'RightSlideMiddle'
    }
</script>


<style scoped>
.right-slide-mid
{
    color:#fff;
	align-items: center;
	display: flex;
	flex-direction: column;
	height: 100%;
	justify-content: center;
	// opacity: 0;
	text-align: center;
	// visibility: hidden;
}
h3
{
	padding: 30px 0;
}
.right-slide-mid
{
	width: 100%;
}
#contact-form
{
	align-items: center;
	display: flex;
	flex-direction: column;
	max-width: 70%;
	width: 100%;
}
.in-area
{
	background: transparent;
	border: none;
	border-bottom: 1px solid #6a6b6a;
	line-height: 30px;
	margin: 10px 0;
	outline: none !important;
	transition: .3s ease-in-out;
	width: 100%;
}
.in-area:focus
{
	border-bottom-color: #fff;
	color: #fff;
}
.in-area::placeholder
{
	color: #fff;
}
.textareas
{
	max-height: 150px;
	min-height: 50px;
	resize: vertical;
}
.sendMsg
{
	background: transparent;
	border: 1px solid #fff;
	cursor: pointer;
	font-size: 30px;
	margin-top: 50px;
	padding: 10px 25px;
	transition: .5s ease-in-out;
    color:#fff;
}
.r-s-close
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
.r-s-close:hover
{
	opacity: 1;
}
img
{
	margin: 0 0;
	margin: 20px 0;
}
span
{
	font-size: 11px;
	letter-spacing: 2px;
	opacity: 0;
	transform: rotate(-90deg);
	width: 40px;
}
</style>