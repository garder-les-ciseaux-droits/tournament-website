<template>  
    <div v-if="burgerMenuShown" class="md:hidden w-full h-full grid grid-cols-1 bg-black absolute right-0 top-0 z-50 overflow-x-hidden">
        <div class="w-full h-full">
            <div class="w-full h-[80px] flex justify-end items-center">
                <button class="w-[40px] h-[40px] rounded-3xl bg-white mr-6" @click="burgerMenu">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" strokeWidth={1.5} stroke="#181818" className="w-6 h-6">
                <path strokeLinecap="round" strokeLinejoin="round" d="M6 18 18 6M6 6l12 12" />
                </svg>
                </button>
            </div>
            <div class="w-full h-[400px] flex items-center justify-start min-w-0">
                    <nav class="w-full h-full mx-10 flex flex-col text-white text-xl font-clash space-y-8 justify-center items-start">
                        <a class="flex w-full h-[50px]">
                            <div class="h-full w-1/2">
                            <p>Tournaments</p>
                            </div>
                            <div class="w-1/2 h-full flex justify-end">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
                            </svg>
                            </div>
                        </a>
                        <a class="flex w-full h-[50px]">
                            <div class="h-full w-1/2">
                            <p>Subscription</p>
                            </div>
                            <div class="w-1/2 h-full flex justify-end">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
                            </svg>
                            </div>
                        </a>
                        <a class="flex w-full h-[50px]">
                            <div class="h-full w-1/2">
                            <p>News</p>
                            </div>
                            <div class="w-1/2 h-full flex justify-end">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
                            </svg>
                            </div>
                        </a>
                        <a class="flex w-full h-[50px]">
                            <div class="h-full w-1/2">
                            <p>Discord</p>
                            </div>
                            <div class="w-1/2 h-full flex justify-end">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="m8.25 4.5 7.5 7.5-7.5 7.5" />
                            </svg>
                            </div>
                        </a>
                    </nav>
            
            </div>
            <div class="w-full h-[150px] flex flex-col text-white font-clash text-xl justify-center items-start mx-10 space-y-8">
                <a class="underline underline-offset-1">Get started</a>
                <a class="underline underline-offset-1">Contact us</a>
                
            </div>
            <div class="w-full h-[100px] flex justify-start justify-center items-center">
                <img class="w-36" src='/src/assets/Images/LOGO.png'/>
            </div>
        </div>
    </div>          
    <div class="w-full h-full bg-[url('/src/assets/background/background.png')] bg-no-repeat bg-contain md:bg-cover bg-center" style="background-position: -70px -70px;">
        <div class="h-[136px] w-full flex justify-center items-center min-w-0">
            <div class="w-[1280px] h-[72px] flex justify-center min-w-0 md:mx-4 mx-10">
                <div class="w-full flex items-center justify-start text-white font-bold text-xl min-w-0">
                    <img class="w-48" src='/src/assets/Images/LOGO.png'/>
                </div>
                <div class="w-full flex items-center justify-center min-w-0">
                    <nav class="hidden md:flex space-x-6 text-white text-sm justify-center items-center">
                        <a>Tournaments</a>
                        <a>Subscription</a>
                        <a>News</a>
                        <a class="flex space-x-1 items-center justify-center">
                            <img class="w-6 h-6" src="/src/assets/Images/discord.png"/>
                            <p>Discord</p>
                        </a>
                    </nav>
            
                </div>
                <div class="inline-block md:hidden w-24 h-full flex justify-center items-center">
                    <button class="inline-block md:hidden w-full h-full flex justify-center items-center" @click="burgerMenu">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="white" class="w-6 h-6">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                            </svg>
                    </button>
                </div>
                <div class="hidden w-full md:flex items-center justify-end text-white">
                    <button class="rounded-3xl text-sm h-10 w-32 bg-gradient-to-r from-[#6600D4] to-[#005FFF]">
                        Get Started
                    </button>
                </div>
            </div>
            
        </div>
        <div class="w-full h-[270px] md:h-[518px] flex justify-center text-white mt-4">
            <div class="w-full md:w-[1280px] h-full min-w-0 md:ml-4 md:mr-4 flex md:mx-0 mx-10">
                <div class="w-full h-[458px] md:w-[640px] md:h-[458px] flex flex-col justify-start space-y-2 md:space-y-4">
                    <div class="w-full min-w-0 min-h-0 md:w-[640px] md:h-[240px] flex flex-col min-w-0 max-w-full">
                        <div class="border border-gray-400 bg-[#272727] rounded-2xl flex w-full md:w-[383px] h-[32px] space-x-2 md:space-x-0 items-center text-white text-xs">
                            <div class="border border-gray-400 rounded-2xl items-center flex h-[24px]">
                                    <img class="pl-1.5" src="/src/assets/Images/_Dot.png"/>
                                    <p class="mx-1.5 text-xs">Featured Tournament</p>
                            </div>
                            <div class="flex">
                                <p>Don't miss out!</p>
                            </div>
                        </div>
                        <div class="w-full h-full md:w-[540px] md:h-[192px] md:flex items-end mt-4 min-w-0 min-h-0">
                            <h1 class="text-white text-2xl md:text-5xl md:leading-tight text-start md:line-clamp-3 font-semibold font-clash drop-shadow-[0_5px_10px_rgba(255,255,255,0.25)]">
                                Experience the Ultimate in Competetive Gaming!
                            </h1>
                        </div>
                    </div>
                    <div class="w-[300px] md:w-[450px] h-[90px] mt-4 flex">
                            <h2 class="text-white text-base md:text-xl text-start text-pretty">
                                Immerse yourself in adrenaline-pumping battles and compete against the best to claim your victory on Tournaments.com today!
                            </h2>
                    </div>
                    <div class="flex items-center md:items-end w-full md:mt-4 h-[80px]">
                        <button class="rounded-3xl w-[200px] h-[42px] md:w-[255px] md:h-[48px] flex justify-center items-center text-white bg-gradient-to-r from-[#6600D4] to-[#005FFF] space-x-3">
                            <p class="text-xs md:text-sm">Compete for Glory Now!</p>
                            <img src="/src/assets/Images/arrow-narrow-right.png"/>
                        </button>
                    </div>
                </div> 
                <div class="hidden md:flex items-center justify-center md:w-[512px] md:h-[518px]">
                    <img class="min-w-[750px] min-h-[400px] mb-14 ml-36 min-w-0 min-w-0" src="/src/assets/background/Image.png">
                </div>
            </div>
        </div>
        <div class="w-full h-[618px] md:h-[256px] flex justify-center items-center md:items-start text-white">
            <div class="w-full md:w-[1280px] h-[480px] md:h-[216px] grid grid-cols-1 justify-center md:space-x-12 md:flex space-y-4 md:space-y-0 min-w-0 mx-10 md:mx-4">
                    <div class="rounded-xl w-full md:w-[656px] min-w-0 h-full flex justify-center items-center space-y-1 bg-gradient-to-r from-white to-black p-0.5">
                        <div class="bg-[url('/src/assets/Images/callofduty.png')] rounded-xl bg-no-repeat bg-cover justify-center items-start bg-center  w-full md:w-[656px] h-[216px] h-full flex flex-col pl-6 pb-4 min-w-0">
                            <h1 class="md:text-3xl font-semibold font-clash w-[244px]">Champion's Early Bird Offer</h1>
                            <h2 class="text-xl w-[288.91px]  h-[46px] font-clash font-medium">Get 10% off your entry free with code: GLORY10</h2>
                        </div>
                    </div>
                    <div class="rounded-xl  w-full lg:w-[656px] min-w-0 h-full flex justify-center space-y-1 bg-gradient-to-r from-white to-black p-0.5">
                        <div class="bg-[url('/src/assets/Images/twoplayers.png')] rounded-xl bg-no-repeat bg-cover justify-center items-start bg-center  w-full lg:w-[656px] h-[216px] h-full flex flex-col pl-6 pb-4 min-w-0">
                            <h1 class="font-semibold font-clash md:text-3xl w-[244px]">Ultimate $50K Winter Cash</h1>
                            <h2 class="text-xl w-[288.91px] h-[46px] font-clash font-medium">Join the frosty fray and come out on top!</h2>
                        </div>
                    </div>
            </div>
        </div>

        <div class="w-full h-[250px] md:h-[300px] flex flex-col md:mt-14 md:justify-center md:items-center">
                <div class="flex w-full h-full justify-center items-center">
                    <div class="flex w-full md:w-[1280px] min-w-0 md:h-[100px] justify-center">
                        <p class="text-white text-1.5xs md:text-lg font-semibold md:mt-3">SUPPORTED BY</p>
                    </div>
                </div>
                <div class="grid grid-cols-2 md:flex w-full h-full">
                    <div class="w-full md:w-[1280px] md:h-[100px] flex min-w-0 justify-center items-center" v-for="sponsor in sponsors" :key="sponsor.id">
                        <div class="justify-center flex items-center w-[170px] h-[48px] space-x-2 min-w-0">
                            <img class="w-6 h-6 md:w-10 md:h-10 min-w-0" :src="`${sponsor.img}`"/>
                            <p class="text-white font-bold min-w-0">{{ sponsor.name }}</p>      
                        </div>       
                    </div>
                </div>
                <div class="w-full h-full flex justify-center items-end">
                    <div class="w-full md:w-[1280px] mb-2 md:mb-0 h-[0px] flex justify-center items-center ml-4 mr-4">
                        <img src="/src/assets/Icons/Divider.png"/>
                    </div>
                </div>

        </div>
    </div>

</template>

<script>
import Boltshift from '/src/assets/Images/SponsorLogos/Boltshift.png'
import FeatherDev from '/src/assets/Images/SponsorLogos/FeatherDev.png'
import VAIONEX from '/src/assets/Images/SponsorLogos/Vaionex.png'
import GlobalBank from '/src/assets/Images/SponsorLogos/GlobalBank.png'
import Nietzsche from '/src/assets/Images/SponsorLogos/Nietzsche.png'

export default {
  data() {
    return {
    
      sponsors: [{name: 'Boltshift', img: Boltshift}, {name:'FeatherDev', img: FeatherDev},{name:'VAIONEX', img: VAIONEX}, {name:'GlobalBank', img: GlobalBank},{name: 'Nietzsche', img: Nietzsche}],
      burgerMenuShown: false,
    }
  },
  methods: {
    burgerMenu(){
        this.burgerMenuShown = !this.burgerMenuShown;
        console.log(this.burgerMenuShown);
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