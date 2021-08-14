<template>
  <div id="app">
    <div id="btn">
    <button @click="changeView">Switch view</button>
    </div>
    <TweetList/>
  </div>
</template>

<script>
import TweetList from './components/TweetList.vue'

export default {
  name: 'App',
  components: {
    TweetList
  },
  methods: {
    changeView() {
      this.$root.$emit('onClick');
    }
  }
}
</script>

<style>
body {
  background-color: rgb(82, 82, 126);
  color: rgb(0, 0, 0);
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
button {
  border-radius: 20px;
}
#btn {
text-align: right;
}

</style>
