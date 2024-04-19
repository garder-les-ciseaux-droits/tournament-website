<template>
  <div class="w-screen h-screen bg-black overflow-y-auto overflow-x-hidden">

    <div class="w-full h-[1150px] md:h-[980px]">
      <HomePage/>
    </div>
    <div class="w-full max-w-full md:h-[1773px] h-[2800px] mt-[150px] md:mt-[470px] lg:mt-[320px] bg-[url('/src/assets/background/background1.png')] bg-no-repeat bg-cover bg-start"  style="background-position: -70px -200px;">
      <HomeBenefits/>
    </div>
    <div class="w-full h-[1800px] md:h-[747px]">
      <FeaturedTournaments/>
    </div>
    <div class="w-full h-[1226px] bg-[url('/src/assets/background/mountain-background-epic-anime--dark-and-perfect-for-gaming--the-feel-is-epic-and-war1.png')] bg-cover bg-center mt-12">
      <ChampionsArena/>
    </div>
    <div class="w-full h-[1600px] md:h-[1146px] bg-[url('/src/assets/background/anotherbg.png')]  bg-center bg-no-repeat"  style="background-position: -0px -40px;">
      <Headline/>
    </div>
    <div class="w-full h-[350.67px] flex flex-col justify-end space-y-16 bg-gradient-to-r from-black via-white to-black">
      
      <TheFooter/>
    </div>
  </div>
  
</template>

<script>
import HomePage from '/src/components/HomePage.vue'
import HomeBenefits from '/src/components/HomeBenefits.vue'
import FeaturedTournaments from '/src/components/FeaturedTournaments.vue'
import ChampionsArena from '/src/components/ChampionsArena.vue'
import Headline from '/src/components/Headline.vue'
import TheFooter from '/src/components/TheFooter.vue'

export default {
  components: {
    HomePage,
    HomeBenefits,
    FeaturedTournaments,
    ChampionsArena,
    Headline,
    TheFooter,
  },
  data() {
    return {
     
    }
  },
  methods: {

  },
  mounted() {
  },
  computed: {

  }

}  

</script>

<style scoped>

</style>
