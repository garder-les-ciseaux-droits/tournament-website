<template>
    <div class="w-full h-[96px] flex justify-center">
        <div class="w-[1280px] h-[96px] flex min-w-0 mx-4">
            <div class="flex flex-col space-y-4 justify-center w-full">
                <h1 class="text-white font-bold text-3xl">Featured Tournaments</h1>
                <h2 class="text-white">Join the fray in your favorite game and claim glory!</h2>
            </div>
            <div class="flex w-full justify-end">
                <button class="text-white rounded-3xl bg-[#212121] w-[191px] h-[48px] flex justify-center items-center space-x-2">
                    <p>All tournaments</p>
                    <img src="/src/assets/Icons/Iconarrowright.png"/>
                </button>
            </div>
        </div>
    </div>
    <div class="w-full h-[505px] flex justify-center items-center mt-10">
        <div class="w-[1280px] h-[505px] flex justify-center  min-w-0 mx-4">
            <div class="w-full h-full md:flex grid grid-cols-1 justify-center space-y-10 md:space-x-14 md:space-y-0  min-w-0">
                <div class="relative w-full h-full flex justify-center min-w-0"  v-for="card in cards" :key="card.id">
                    <div class="w-full md:w-[384px] h-[505px] flex rounded-xl items-end min-w-0" :style="defineTheBackground(card.img)">
                        
                        <div class="w-full h-[192px] flex justify-center items-center min-w-0">
                            
                            <div class="bg-gradient-to-b from-transparent to-black w-full md:w-full h-[200px] md:h-full flex flex-col justify-center items-center space-y-2 min-w-0 pb-4 md:pb-0">
                                <div class="md:w-[320px] md:h-[200px] w-[400px] h-full flex flex-col justify-center items-center min-w-0 max-w-full space-y-2">
                                    <h1 class="text-white text-2xl font-bold leading-8 text-balance w-full">{{ card.title }}</h1>
                                    <h1 class="text-white text-xl font-light text-balance leading-7 w-full">{{ card.description }}</h1>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
            </div>
        </div>

    </div>
</template>

<script>
export default {
  data() {
    return {
        cardImg: '',
        cards: [{title: 'Valorant Victory Rush', description: 'Dominate the Arena for a $50K Prize Pool!', img: '/tournament-website/src/assets/Images/65bfe9ad060a66d706890833818a2260.png'}, 
                {title: 'Call of Duty: Combat Challenge', description: 'Deploy and Conquer for $30K in Cash & Gear!', img: '/tournament-website/src/assets/Images/65bfe9ad060a66d706890833818a22602.png'}, 
                {title: 'Apex Legends: Champions Quest', description: 'Outlast the Legends to Win $20K + Exclusive Items!', img: '/tournament-website/src/assets/Images/65bfe9ad060a66d706890833818a22603.png'}]
    }
  }, 
  methods: {
    defineTheBackground(card){
        return `background-image: url(${card}); background-position: center; background-size: cover;`;
    }
  },
  mounted() {
  },
  computed: {

  }

}  

</script>

<style>

</style>