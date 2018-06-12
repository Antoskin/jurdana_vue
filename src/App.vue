<template>
  <div id="app">
   <LeftSlide></LeftSlide>
    <RightSlide></RightSlide>
    <MainWrap></MainWrap>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import LeftSlide from './components/Sliders/SliderLeft/SlideLeft'
import RightSlide from './components/Sliders/SliderRight/SlideRight'
import MainWrap from './components/CentralMain/MainWrap'

export default {
  name: 'App',
  components: {
    LeftSlide,
    RightSlide,
    MainWrap
  }
}
</script>

<style>
@import '../node_modules/reset-css/sass/_reset.scss';

#app {
    width: 100%;
    display: flex;
    height: 100%;
    position: fixed;
}
</style>
