<template>
  <div id="app" class="font-hairline text-base font-sans tracking-normal leading-loose bg-grey-light h-full">
    <TheHeader />
    <main class="app-content container">
      <div class="flex flex-wrap my-6 -mx-2">
        <div class="w-full sm:w-full md:w-full lg:w-2/3 px-2">
          <h2 class="font-normal text-grey-darkest text-xl tracking-wide my-12">Leaderboard</h2>
          <table class="leaderboard text-black">
            <thead class="bg-green">
              <tr>
                <th class="p-5 font-light">Place</th>
                <th class="p-5 font-light">Team Name</th>
                <th class="p-5 font-light">Macthes played</th>
                <th class="p-5 font-light">Wins</th>
                <th class="p-5 font-light">Lost</th>
                <th class="p-5 font-light">Points</th>
              </tr>
            </thead>
            <tbody>
              <tr class="bg-white" v-for="team in teams" :key="team.id">
                <td class="p-5 text-black font-semibold"> {{ team.place }}</td>
                <td class="p-5">{{ team.name }}</td>
                <td class="p-5">{{ team.matchesPlayed }}</td>
                <td class="p-5">{{ team.matchesWon }}</td>
                <td class="p-5">{{ team.matchesLost }}</td>
                <td class="p-5">{{ team.points }}</td>
              </tr>
            </tbody>
          </table>
        </div>
        <div class="w-full sm:w-full md:w-full lg:w-1/3 px-2">
          <h2 class="font-normal text-grey-darkest text-xl tracking-wide my-12">Match overview</h2>
            <MatchOverview />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import './assets/styles/main.css'
import TheHeader from './components/TheHeader'
import MatchOverview from './components/MatchOverview'

export default {
  name: 'App',
  components: {
    TheHeader,
    MatchOverview,
  },
  data(){
    return {
      teams: [
        {
          id: 1,
          place: 1,
          name: 'Team-1',
          matchesPlayed: 3,
          matchesWon: 1,
          matchesLost: 2,
          points: 3
        },
        {
          id: 2,
          place: 2,
          name: 'Team-2',
          matchesPlayed: 3,
          matchesWon: 1,
          matchesLost: 2,
          points: 3
        },
        {
          id: 3,
          place: 3,
          name: 'Team-3',
          matchesPlayed: 10,
          matchesWon: 2,
          matchesLost: 3,
          points: 3
        },
        {
          id: 4,
          place: 4,
          name: 'Team-4',
          matchesPlayed: 90,
          matchesWon: 3,
          matchesLost: 2,
          points: 123
        },
        {
          id: 5,
          place: 5,
          name: 'Team-5',
          matchesPlayed: 15,
          matchesWon: 10,
          matchesLost: 2,
          points: 10,
        },
        {
          id: 6,
          place: 6,
          name: 'Team-5',
          matchesPlayed: 3,
          matchesWon: 1,
          matchesLost: 2,
          points: 10
        },
        {
          id: 7,
          place: 7,
          name: 'Team-7',
          matchesPlayed: 3,
          matchesWon: 1,
          matchesLost: 2,
          points: 3
        },
        {
          id: 8,
          place: 8,
          name: 'Team-8',
          matchesPlayed: 3,
          matchesWon: 1,
          matchesLost: 2,
          points: 3
        }
      ]
    }
  },
}
</script>

<style>

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
