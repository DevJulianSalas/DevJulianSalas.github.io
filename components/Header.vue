<template>
  <div>
    <el-row
      type="flex"
      class="header"
    >
      <el-col :span="4" :x12="12">
        <img src="../assets/logo2.svg" alt="logjs" class="brand">
      </el-col>
      <el-col :span="20">
        <Menu />
      </el-col>
    </el-row>
    <el-row
      type="flex"
      class="welcome-message"
    >
      <el-col class="message-front" :span="24" :xs="12">
        Hello! <br>I'm a fullstack developer<span style="color:#f95231">
          .
        </span>
        <p style="text-transform: lowercase;">I am an enthusiastic and motivated full stack that enjoys solving challenges and share knowledge with other people & I am a lover of learning new technologies to apply in projects.</p>
      </el-col>
    </el-row>
  </div>
</template>
<script>
import Menu from '../components/Menu'
export default {
  components: {
    Menu
  }
}
</script>
<style scoped>
.header {
  display: flex;
  flex-flow: row wrap;
  align-items: center;
  align-content: flex-end;
  width: 100%;
}
.brand {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 60%;
  height: 50%;
}

.welcome-message {
  flex-flow: row wrap;
  align-items: center;
  padding-top: 50px;
}

.message-front {
  font-family: 'Poppins', sans-serif;
  font-size: 40px;
  font-weight: 700;
  color: #11242c;
  line-height: 1.8em;
  text-align: center;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}

p {
  font-size: 22px;
  color: #203b4c;
  font-weight: 300;
  line-height: 1.5em;
  text-align: center;
  margin-left: auto;
  margin-right: auto;
  width: 100%;
}
</style>
