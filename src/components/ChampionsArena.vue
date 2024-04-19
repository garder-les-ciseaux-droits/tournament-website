<template>
    <div class="w-full h-[96px] flex justify-center">
        <div class="w-[1280px] h-[96px] min-w-0 mx-10 md:mx-4">
            <div class="flex flex-col space-y-4 justify-center w-full items-center">
                <h1 class="text-white font-bold text-3xl md:text-5xl">Champions of the Arena</h1>
                <h2 class="text-white text-xl font-light">Meet the elite players dominating the game</h2>
            </div>
        </div>
    </div>
    <div class="w-full h-full flex justify-center mt-14">
        <div class="w-[1280px] h-[964px] min-w-0 mx-10 md:mx-4">
            <div class="w-full h-[44px] border rounded-xl border-gray-600 bg-gradient-to-r from-black/70 to-[#212121]/70 flex">
                <div class="h-full w-[80px] md:w-[102px] text-white flex justify-center items-center">
                    <p class="md:text-base text-xs">Rank</p>
                </div>
                <div class="h-full w-[222.8px] text-white flex justify-start items-center ml-4">
                    <p class="md:text-base text-xs">Leaders Name</p>
                </div>
                <div class="h-full w-[222.8px] text-white flex justify-center items-center">
                    <button class="flex items-center md:text-base text-xs" @click="sortedPlayers('winRate')">
                        Win Rate
                        <img class="w-[12px] h-[12px] md:w-[16px] md:h-[16px]" src="/src/assets/Icons/chevron-selector-vertical.png"/>
                    </button>
                    
                </div>
                <div class="h-full w-[222.8px] text-white flex justify-center items-center">
                    <button class="flex items-center md:text-base text-xs" @click="sortedPlayers('tournamentWins')">
                        Tournament Wins
                        <img class="w-[12px] h-[12px] md:w-[16px] md:h-[16px]" src="/src/assets/Icons/chevron-selector-vertical.png"/>
                    </button>
                </div>
                <div class="h-full w-[222.8px] text-white flex justify-center items-center space-x-1">
                    <button class="flex items-center md:text-base text-xs" @click="sortedPlayers('topThree')">
                        Top 3 Finishes
                        <img class="w-[12px] h-[12px] md:w-[16px] md:h-[16px]" src="/src/assets/Icons/chevron-selector-vertical.png"/>
                    </button>
                    
                </div>
                <div class="h-full w-[222.8px] text-white justify-center items-center md:space-x-1 hidden md:flex">
                    <button class="flex items-center md:text-base text-xs"  @click="sortedPlayers('topEight')">
                        <p>Top 8 Finishes</p>
                        <img class="w-[12px] h-[12px] md:w-[16px] md:h-[16px]" src="/src/assets/Icons/chevron-selector-vertical.png"/>
                    </button>
                </div>
            </div>
            <div class="w-full mt-6" v-for="(player, index) in topTenPlayers" :key="player.id">
                <div class="w-full h-[72px] border rounded-xl border-gray-600 bg-gradient-to-r from-black/70 to-[#212121]/70  flex">
                    <div class="h-full w-[80px] md:w-[102px] text-white flex justify-center items-center">
                        <p class="md:text-lg text-xs">{{ index + 1 }}</p>
                    </div>
                    <div class="h-full w-[222.8px] overflow-x-auto md:overflow-x-hidden text-white flex justify-start items-center space-x-3 ml-4">
                        <div class="w-[20px] h-[20px] md:w-[40px] md:h-[40px]">
                            <img class="rounded-3xl  w-full h-full" :src="player.avatar"/>
                        </div>
                        <p class="md:text-lg text-xs text-balance truncate">{{ player.name }}</p>
                    </div>
                    <div class="h-full w-[222.8px] text-white flex justify-center items-center">
                        <p class="md:text-lg text-xs">{{ player.winRate + '%' }}</p>
                    </div>
                    <div class="h-full w-[222.8px] text-white flex justify-center items-center">
                        <p class="md:text-lg text-xs">{{ player.tournamentWins }}</p>
                    </div>
                    <div class="h-full w-[222.8px] text-white flex justify-center items-center">
                        <p class="md:text-lg text-xs">{{ player.topThree }}</p>
                    </div>
                    <div class="h-full w-[222.8px] hidden md:flex text-white justify-center items-center">
                        <p class="md:text-lg text-xs hidden md:flex">{{ player.topEight }}</p>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>


<script>
import Avatar from '/src/assets/Images/PlayersIcons/Avatar.png'
import Avatar8 from '/src/assets/Images/PlayersIcons/Avatar8.png'
import Avatar2 from '/src/assets/Images/PlayersIcons/Avatar2.png'
import Avatar3 from '/src/assets/Images/PlayersIcons/Avatar3.png'
import Avatar7 from '/src/assets/Images/PlayersIcons/Avatar7.png'
import Avatar4 from '/src/assets/Images/PlayersIcons/Avatar4.png'
import Avatar5 from '/src/assets/Images/PlayersIcons/Avatar5.png'
import Avatar6 from '/src/assets/Images/PlayersIcons/Avatar6.png'


export default {
  data() {
    return {
        topTenPlayers: [{name: 'Phantom Blade', winRate: 89, tournamentWins: 11, topThree: 7, topEight: 0, avatar: Avatar}, {name: 'RavenYeager', winRate: 88, tournamentWins: 2, topThree: 5, topEight: 4, avatar: Avatar8}, {name: 'PawsMaster', winRate: 87, tournamentWins: 7, topThree: 4, topEight: 1, avatar: Avatar2}, {name: 'FingerWarrior', winRate: 83, tournamentWins: 9, topThree: 9, topEight: 6, avatar: Avatar3}, {name: 'IronHead', winRate: 80, tournamentWins: 1, topThree: 2, topEight: 8, avatar: Avatar7}, {name: 'QuantumKaizen', winRate: 80, tournamentWins: 1, topThree: 8, topEight: 8, avatar: Avatar4}, {name: 'EchoPulse', winRate: 75, tournamentWins: 0, topThree: 3, topEight: 0, avatar: Avatar5}, {name: 'Blitz', winRate: 72, tournamentWins: 1, topThree: 5, topEight: 9, avatar: Avatar6}, {name: 'SilverEdge', winRate: 71, tournamentWins: 3, topThree: 6, topEight: 12, avatar: Avatar5}, {name: 'Notyourbae', winRate: 70, tournamentWins: 5, topThree: 1, topEight: 6, avatar: Avatar5}],
    }
  },
  methods: {
    sortedPlayers(key){
        let sorted = this.topTenPlayers.reduce(function(acc, current){
        let inserted = false;

        for(let i = 0; i < acc.length; i++){
            if(current[key] > acc[i][key]){
                acc.splice(i, 0, current);
                inserted = true;
                break;
            }
        }
        if(!inserted){
            acc.push(current)
        }
            return acc;
        }, []);

        this.topTenPlayers = sorted;
        console.log(this.topTenPlayers);
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