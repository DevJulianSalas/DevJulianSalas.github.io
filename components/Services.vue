<template>
  <div>
    <SubHeader 
      subheader="What i love to do"
      :subtext="myServices"
    />
    <el-row
      type="flex"
      justify="center"
      style="flex-flow: row wrap; margin: 60px; padding-top:20px;"
    >
      <el-col
        v-for="(item, index) in services"
        :key="index"
        :span="6"
        style="text-align: center;"
      >
        <div style="margin: 20px;">
          <i :class="item.icon" style="width: 42px; height: 42px; color: #42b883;"/>
          <p style="color: #11242c;">{{ item.name }}</p>
          <!-- <p>{{ item.description }}</p> -->
        </div>
      </el-col>
    </el-row>
  </div>
</template>
<script>
import SubHeader from './SubHeader'
export default {
  components: {
    SubHeader
  },
  data: function() {
    return {
      myServices: 'lorem lorel lorem',
      services: [
        {
          name: 'Backend',
          icon: 'fas fa-server',
          description: `Let me create scalable backends with the best stack.`
        },
        {
          name: 'Frontend',
          icon: 'fas fa-terminal',
          description: `Let me create amazing and fast UI interfaces with javascript.`
        },
        {
          name: 'Apps',
          icon: 'fas fa-mobile-alt',
          description: `Let me create apps multiplaform `
        },
        {
          name: 'IoT',
          icon: 'fas fa-wifi',
          description: `Fringilla augue at maximus vesti Nam pulvinar vitae neque etrolling freight.`
        }
      ]
    }
  }
}
</script>
<style scoped>
.services {
  display: flex;
  flex-flow: row wrap;
}
h2 {
  color: #11242c;
  margin: 0 0 10px;
  text-transform: none;
  font-weight: 500;
  font-family: 'Montserrat', sans-serif;
  font-size: 200%;
  letter-spacing: -1px;
}
</style>
