<template>
  <div class="container">
    <header class="header">
      <Header />
    </header>
    <section class="main">
      <p>prueba main</p>
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

h2 {
  font-family: 'Dosis', sans-serif !important;
  color: #232332;
  font-weight: 500;
  letter-spacing: 5px;
}

p {
  font-size: 14px;
  font-weight: normal;
  line-height: 24px;
  color: #555;
  margin-bottom: 15px;
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
