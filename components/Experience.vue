<template>
  <div>
    <SubHeader
      subheader="My experience"
      :subtext="experienceText"
    />
    <el-row
      type="flex"
      class="step-experience"
    >
      <el-col 
        :span="24"
        class="step-col"
      >
        <el-steps 
          :key="index"
          direction="vertical"
          :space="160"
          class="step-col"
        >
          <el-step 
            v-for="(item, index) in experience"
            :key="index"
            icon="el-icon-circle-plus-outline"
          >
            <div slot="title">
              <div class="step-title">
                <span style="color: #555; flex: 1;">
                  {{ item.datetime }}
                </span>
                <span style="color: #11242c; font-size: 20px; text-transform: capitalize; font-weight: 500; flex: 1;">
                  <a 
                    style="color: rgb(17, 36, 44); font-size: 20px; text-transform: capitalize; font-weight: 500;" 
                    :href="item.site" 
                    target="_blank" 
                    rel="noopener noreferrer"
                  >
                    {{ item.company }}
                  </a>
                </span><br>
                <br>
              </div>
            </div>
            <div slot="description">
              <div class="step-subtitle">
                <span style="color: #555; font-size: 14px; text-transform: capitalize; font-weight: 500;">
                  {{ item.role }}
                </span>
              </div>
            </div>
            <div slot="icon">
              <i style="color: #42b883;" class="el-step__icon-inner el-icon-circle-plus-outline" />
            </div>
          </el-step>
        </el-steps>
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
      experienceText: `
        I have worked in cool companies of which I have learned so much and allowed me to growth personally and professionally.
      `,
      experience: [
        {
          datetime: 'jun 2017 - present',
          company: 'xprende',
          role: 'fullstack developer',
          site: 'https://demo.xprende.com'
        },
        {
          datetime: 'dec 2017 - present',
          company: 'infobibliotecas - Efilm',
          role: 'fullstack developer',
          site: 'https://efilm.online/'
        },
        {
          datetime: 'Aug 2017 - Sep 2017',
          company: 'tinkulab',
          role: 'fullstack developer'
        },
        {
          datetime: 'Jan 2016 - Oct 2017',
          company: 'pitmmam',
          role: 'backend developer',
          site: 'https://www.pitmmam.com/'
        },
        {
          datetime: 'Aug 2014 - Dec 2015',
          company: 'Institute Technology Metropolitan',
          role: 'Laboratory Manager',
          site: 'https://www.itm.edu.co/dependencias/centro-de-laboratorios/'
        }
      ]
    }
  }
}
</script>
<style scoped>
.step-experience {
  flex-flow: row wrap;
  justify-content: center;
  margin: 40px;
  padding-top: 40px;
}
.step-title {
  display: flex;
  text-transform: uppercase;
  margin: 10px;
}
.step-subtitle {
  display: flex;
  flex-flow: column wrap;
  margin: 10px;
}
.step-col {
  display: flex;
  flex: 0.7;
  justify-content: center;
  align-content: center;
}
</style>
