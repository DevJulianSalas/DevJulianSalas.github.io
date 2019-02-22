<template>
  <div>
    <SubHeader
      subheader="My awesome projects"
      :subtext="myProjectsText"
    />
    <el-row
      type="flex"
      class="my-projects"
    >
      <el-col 
        v-for="(item, index) in projects"
        :key="index"
        :span="9"
        style="width: 48%"
      >
        <el-card 
          :body-style="{ padding: '0px'}"
          class="card-whole"
          shadow="hover"
        >
          <div class="body-project">
            <span style="color: #11242c; font-size: 20px; text-transform: capitalize; font-weight: 500; flex: 1;">
              {{ item.Title }}
            </span><br>
            <p style="padding-top: 5px; margin-bottom: 0px">
              {{ item.description }}
            </p><br>
            <div style="display: flex;">
              <span style="color: #11242c; text-transform: capitalize; font-weight: 400; flex: 1;">
                {{ item.role}}
              </span>
              <el-tooltip class="item" effect="dark" :content="item.topic" placement="top-start">
                <span style="color: #11242c; text-transform: capitalize; font-weight: 400; text-align: right;">
                  <i :class="item.icon" style="width: 22px; height: 22px; color: #42b883;" />
                </span>
              </el-tooltip>
            </div>
          </div>
        </el-card>
      </el-col>
      <el-col :span="24" style="">
        <div style="display: flex;">
          <span style="flex: 1; text-align: right; padding-right: 40px">
            <nuxt-link style="color: #42b883; font-size: 18px; text-transform: capitalize; font-weight: 400;" to="/projects">See more</nuxt-link>
          </span>
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
      myProjectsText: `I am constantly looking for either open source projects where i can contributed or private projects. If you have one in mind just write me I will be so happy to support you.`,
      projects: [
        {
          Title: 'Xprende.',
          description: `
            A virtual learning platform that allow as a user take on courses and as a management create amazing courses with pre-fabric componentes like video, images, text or drap and drop ...
          `,
          role: 'FullStack Developer',
          topic: 'Web development - SPA',
          icon: 'fas fa-globe'
        },
        {
          Title: 'Efilm.',
          description: `
            An online streaming platform which was created exclusively to users belong to subscribed libraries, those users can enjoy the amazing content like concerts, cine, series or audiovisuals..
          `,
          role: 'FullStack Developer',
          topic: 'Web development',
          icon: 'fas fa-globe'
        },
        {
          Title: 'Measurement system of humidity and temperature.',
          description: `
            An open source project with an embedded system built with nodecmu chip and DHT22 sensor which can being make by your-self to get home data, and then analyze and show the behaviour in real time.
          `,
          role: 'FullStack Developer',
          topic: 'Internet of things, embedded system',
          icon: 'fas fa-wifi'
        },
        {
          Title: 'Ticket system dashboard',
          description: `
            A system which can help you to track and deal issues/incidents in your private organization moreover it has a interactive dashboard with important metrics to the admins.
          `,
          role: 'FullStack Developer',
          topic: 'Web development - SPA',
          icon: 'fas fa-globe'
        }
      ]
    }
  }
}
</script>
<style scoped>
.my-projects {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-evenly;
  padding-top: 25px;
}

.card-whole {
  height: 180px;
  width: 90%;
  margin: 30px;
  border-bottom: 3px solid #42b883;
}
.body-project {
  padding: 25px;
}
</style>
