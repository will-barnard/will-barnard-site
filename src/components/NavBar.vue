<template>
    <nav>
        <h3 v-on:click="goHome">Home</h3>
        <h3 v-on:click="goAbout">About</h3>
      </nav>
</template>


<script>

export default {
    methods: {
      goHome() {
        this.$router.push({name: 'home'});
      },
      goAbout() {
        this.$router.push({name: 'about'})
      }
    }
}
</script>


<style scoped>
h3 {
  cursor: pointer;
}
</style>