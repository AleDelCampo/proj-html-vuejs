<script>
import Slider from './components/Slider.vue';
import Header from './components/Header.vue';
import UpcomingMatches from './components/UpcomingMatches.vue';
import PlayerCards from './components/PlayerCards.vue';
import Table from './components/Table.vue';
import Sponsors from './components/Sponsors.vue';

export default {
  components: {
    Slider,
    Header,
    UpcomingMatches,
    PlayerCards,
    Table,
    Sponsors
  },
}
</script>


<template>
  <div>
    <Slider></Slider>
    
    <Header></Header>

    <UpcomingMatches></UpcomingMatches>

    <PlayerCards></PlayerCards>

    <Table></Table>

    <Sponsors></Sponsors>
  </div>
</template>


<style lang="scss">
</style>