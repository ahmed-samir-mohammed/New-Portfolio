<template>
  <div class="home">
    <h1>When everything else fails read the instructions.</h1>
    <h2>Ahmed Samir</h2>
    <p>UI/UX Designer && Front-End Developer</p>
  </div>
</template>

<script>
// @ is an alias to /sr

export default {
  name: 'home',

}
</script>

<style lang="scss">
  .home {
    width: 100%;
    height: 93vh;
    padding: 3rem;
    background: rgba(0, 0, 0, 0.8) !important;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    h1 {
      font-size: 3rem;
    }
    h2 {
      font-size: 2rem
    }
  }
</style>
