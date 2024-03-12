<script>
import Slider from './components/Slider.vue';
import Header from './components/Header.vue';
import UpcomingMatches from './components/UpcomingMatches.vue';
import PlayerCards from './components/PlayerCards.vue';
import Table from './components/Table.vue';
import Sponsors from './components/Sponsors.vue';
import News from './components/News.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    Slider,
    Header,
    UpcomingMatches,
    PlayerCards,
    Table,
    Sponsors,
    News,
    Footer
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

    <News></News>

    <Footer></Footer>
  </div>
</template>


<style lang="scss">
</style>