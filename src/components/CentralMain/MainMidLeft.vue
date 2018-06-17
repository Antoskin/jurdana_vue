<template>
        <div class="middle-sib middle-left">
                        <div @click="openSlideL" class="btn-wrap btn-left">
                            <div class="dots">
                                <span class="dot dot-one"></span>
                                <span class="dot dot-two"></span>
                                <span class="dot dot-three"></span>
                            </div>
                            <p class="btn-text">OUR SERVICES</p>
                        </div>
        </div>
</template>


<script>
	
	import { bus } from '../../main.js'

    export default {
        name: 'MainMidLeft',
        methods: {
        	openSlideL() {
        		bus.$emit('slideOpenL')
        	}
        }

    }
</script>


<style scoped>
    .middle-sib {
	width: 300px;
	display: flex;
	align-items: center;
}

.middle-sib .btn-wrap {
	display: flex;
	align-items: center;
	width: 100%;
	cursor: pointer;
}

.middle-sib .btn-wrap:hover .dot {
	animation: inherit !important;
}

.middle-sib .btn-wrap:hover .btn-text {
	opacity: 1;
}

.middle-sib .btn-wrap .dots {
	width: 40px;
	display: flex;
	justify-content: space-between;
	align-items: center;
}

.middle-sib .btn-wrap .dots .dot {
	border-radius: 50%;
	background: #fff;
	//animation: biSmall 3s infinite;
}

.middle-sib .btn-wrap .dots .dot-one {
	width: 13px;
	height: 13px;
	animation-delay: .4s;
}

.middle-sib .btn-wrap .dots .dot-two {
	width: 9px;
	height: 9px;
	animation-delay: .2s;
}

.middle-sib .btn-wrap .dots .dot-three {
	width: 6px;
	height: 6px;
}

.middle-sib .btn-wrap .btn-text {
	letter-spacing: 3px;
	transition: .3s ease-in-out;
	margin: 0 10px;
}
</style>