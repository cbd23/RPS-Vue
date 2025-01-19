<script setup>
import Header from './components/Header.vue';
import Main from './components/Main.vue';

function getRoundResult(humanChoice) {
    console.log('You choosed ' + humanChoice)
}
</script>

<template>
  <Header></Header>
  <Main @play-round="getRoundResult"></Main>
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
