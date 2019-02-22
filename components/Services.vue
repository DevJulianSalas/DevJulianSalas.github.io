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
          <i :class="item.icon" style="width: 42px; height: 42px; color: #42b883;" />
          <p style="color: #11242c; margin-bottom: 20px;">
            {{ item.name }}
          </p>
          <p>
            {{ item.description }}
          </p>
          <p style="color: #42b883; margin-top: 20px; margin-bottom: 40px;">
            Stack I speak:
          </p>
          <div 
            v-for="(stack, indexStack) in item.stack"
            :key="indexStack"
            style="padding-top: 2px;"
          >
            <p>
              {{ stack }}
            </p>
          </div>
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
      myServices: `
        Do you have an idea in mind? guess what, I love coding and materialising ideas with the best stack that allow you a quickly scaling.
      `,
      services: [
        {
          name: 'Backend',
          icon: 'fas fa-server',
          description: `Let me create a trusly and scalable service to response   .`,
          stack: [
            'Django postgres',
            'Flask mongodb',
            'Express mongodb',
            'Firebase'
          ]
        },
        {
          name: 'Frontend',
          icon: 'fas fa-terminal',
          description: `Let me build a truly, lightweight and friendly User Interface to allow the clients know about you and your amazing products.`,
          stack: [
            'Javascript',
            'VueJs Ecosystem',
            'Nuxtjs',
            'ReactJs Ecosystem'
          ]
        },
        {
          name: 'Apps',
          icon: 'fas fa-mobile-alt',
          description: `Let me create you a great cross-platform app to improve your business brand and keep up the clients updated with push notifications.`,
          stack: [
            'Javascript',
            'React Native Ecosystem',
            'NativeBase',
            'Learning Flutter :)'
          ]
        },
        {
          name: 'IoT',
          icon: 'fas fa-wifi',
          description: `Let me meassurement, process and analyze interesting data to the clients and show in amazing UI dashboards.`,
          stack: ['Embedded Devices', 'smart sensors', 'Arduino', 'NodeCmu']
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
