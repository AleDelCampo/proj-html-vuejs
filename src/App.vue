<script>
import Slider from './components/Slider.vue';
import Header from './components/Header.vue';
import UpcomingMatches from './components/UpcomingMatches.vue';
import PlayerCards from './components/PlayerCards.vue';

export default {
  components: {
    Slider,
    Header,
    UpcomingMatches,
    PlayerCards
  },
}
</script>


<template>
  <div>
    <Slider></Slider>
    
    <Header></Header>

    <UpcomingMatches></UpcomingMatches>

    <PlayerCards></PlayerCards>
  </div>
</template>


<style lang="scss">
</style>