<template>
    <div class="central-block">
            <div class="central-block_wrap">
				<MainTop></MainTop>
                <MainMid></MainMid>
                <MainBot></MainBot>
            </div>
    </div>
</template>

<script>
	import MainTop from './MainTop'
	import MainMid from './MainMid.vue'
	import MainBot from './MainBot.vue'
    export default {
        name: 'MainWrap',
		components: {
			MainTop,
			MainMid,
			MainBot
		}
    }
</script>


<style scoped>
.central-block {
	position: absolute;
	top: 55px;
	left: 90px;
	right: 90px;
	bottom: 55px;
}

.central-block .central-block_wrap {
	width: 100%;
	height: 100%;
	position: relative;
	display: flex;
	flex-direction: column;
}
</style>