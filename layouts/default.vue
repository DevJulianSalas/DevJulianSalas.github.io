<template>
  <div class="container">
    <header class="header">
      <Header />
    </header>
    <section class="main">
      <nuxt />
    </section>
    <footer>
      <p>footer</p>
    </footer>
  </div>
</template>
<script>
import Header from '../components/Header'
export default {
  components: {
    Header
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

.header {
  height: 500px;
  width: 100%;
}

.main {
  width: 100%;
  flex: 1;
}
</style>
