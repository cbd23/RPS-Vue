<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
  },
  data() {
    return {
      computerChoice: '',
      roundResult: '',
    };
  },
  methods: {
    getComputerChoice() {
      let randomNumber = Math.floor(Math.random() * 3)

      if (randomNumber === 0) {
        this.computerChoice = 'rock'
      } else if (randomNumber === 1) {
        this.computerChoice = 'paper'
      } else this.computerChoice = 'scissors'

      return this.computerChoice
    },
    getRoundResult(humanChoice) {

      this.getComputerChoice()

      console.log('You chose ' + humanChoice)
      console.log('Computer chose ' + this.computerChoice)

      // TIE case:
      if (humanChoice === this.computerChoice) {
        this.roundResult = 'TIE'
      }

      // 'HUMAN WON' cases:
      else if (humanChoice === 'rock' && this.computerChoice === 'scissors') {
        this.roundResult = 'HUMAN WON'
      } else if (humanChoice === 'paper' && this.computerChoice === 'rock') {
        this.roundResult = 'HUMAN WON'
      } else if (humanChoice === 'scissors' && this.computerChoice === 'paper') {
        this.roundResult = 'HUMAN WON'
      } 
      
      // Anything else means 'HUMAN LOST'
      else this.roundResult = 'HUMAN LOST'

      console.log(this.roundResult)
      return this.roundResult
    },
  },
}
</script>

<template>
  <Header></Header>
  <Main @play-round="getRoundResult" :roundResult="roundResult"></Main>
</template>

<style scoped>


body {
  border: 1px solid orange;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>
