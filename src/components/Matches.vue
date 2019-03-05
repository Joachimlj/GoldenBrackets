<template>
  <ul class="app-content__match-overview-list list-reset">
    <li class="app-content__match-overview-list__item flex justify-between mb-5 bg-white p-5 shadow" v-for="match in matches" :key="match.id">      
      <span>{{ match[0].teamName }}</span> <span class="match__result bg-black text-white px-4 font-medium">{{ match[0].score }} : {{ match[1].score }}</span> <span>{{ match[1].teamName }}</span>
    </li>
  </ul>
</template>

<script>

export default {
  name: 'Matches',
  data () {
    return {
      matches: [
        [
          {
            id: 1,
            teamName: 'TeamA',
            score: 0,
            wins: 1,
          },
          {
            id: 2,
            teamName: 'TeamB',
            score: 3,
            wins: 3,
          },
        ],
        [
          {
            id: 3,
            teamName: 'TeamC',
            score: 0,
            wins: 5,
          },
          {
            id: 4,
            teamName: 'TeamD',
            score: 3,
            wins: 0,
          },
        ],
        [
          {
            id: 5,
            teamName: 'TeamE',
            score: 3,
            wins: 10,
          },
          {
            id: 6,
            teamName: 'TeamF',
            score: 3,
            wins: 0,
          },
        ],
        [
          {
            id: 6,
            teamName: 'TeamG',
            score: 3,
            wins: 9,
          },
          {
            id: 7,
            teamName: 'TeamH',
            score: 3,
            wins: 11,
          },
        ],
      ],
    }
  }
}
</script>

<style scoped>

</style>
