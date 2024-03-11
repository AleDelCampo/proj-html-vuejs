<script>
import Slider from './components/Slider.vue';
import Header from './components/Header.vue';
import UpcomingMatches from './components/UpcomingMatches.vue';

export default {
  components: {
    Slider,
    Header,
    UpcomingMatches
  },
}
</script>


<template>
  <div>
    <Slider></Slider>
    
    <Header></Header>

    <UpcomingMatches></UpcomingMatches>
  </div>
</template>


<style lang="scss">
</style>