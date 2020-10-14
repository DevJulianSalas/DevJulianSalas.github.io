<template>
  <div class="main-background">
    <div class="main-box">
      <img src="../assets/logo2.svg" alt="logjs" class="brand">
      <h1 class="main-text">Coming Soon</h1>
    </div>
    <!-- <Header />
    <section class="main">
      <nuxt />
    </section>
    <footer style="height: 50px; background: #35495e;">
      <div style="display: flex; flex-flow: row wrap; align-items: center; justify-content: flex-end;">
        <span style="color: #ffffff; margin: 10px; text-transform: capitalize; font-weight: 500">
          Made <i class="fas fa-heart" style="width: 22px; height: 22px; color: #42b883;"/> 
          with <span>
            <a style="color: #ffffff; margin: 0px; padding: 2px;" href="https://nuxtjs.org" target="_blank" rel='noopener noreferrer'>
              Nuxtjs
            </a></span> by <span>Julian Salas.</span>
        </span>
      </div>
    </footer> -->
  </div>
</template>
<script>
// import Header from '../components/Header'
export default {
  components: {
    // Header
  }
}
</script>

<style>
html {
  font-family: 'Poppins', sans-serif;
  /* font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif; */
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
* {
  padding: 0%;
  margin: 0%;
  box-sizing: border-box;
}

p {
  font-size: 14px;
  font-weight: normal;
  line-height: 24px;
  color: #555;
  margin-bottom: 15px;
}

ul {
  list-style-type: none;
}

a {
  text-decoration: none;
  text-transform: uppercase;
  font-size: 13px;
  color: #082639;
  font-family: 'Poppins', sans-serif;
  padding: 20px;
  font-weight: 10;
}

h2 {
  color: #11242c;
  margin: 0 0 10px;
  text-transform: none;
  font-weight: 400;
  font-family: 'Montserrat', sans-serif;
  font-size: 240%;
  letter-spacing: -1px;
}

.container {
  display: flex;
  flex-flow: row wrap;
}

.container > * {
  flex: 1 100%;
}

.main {
  width: 100%;
  flex: 1;
}

.main-background {
  width: 100%;
  height: 100vh;
  display: flex;
  background-color: #f5f5f5;
  justify-content: center;
  align-items: center;
}

.main-box {
  width: 45%;
  height: 45%;
  background-color: #4db6ac;
}
.brand {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 60%;
  height: 50%;
}

.main-text {
  color: white;
  text-align: center;
  padding-top: 10px;
}
</style>
