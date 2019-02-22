<template>
  <div>
    <SubHeader
      subheader="my awesome projects"
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
              Diploma in Information Technology
            </span><br>
            <p style="padding-top: 10px;">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do iusmodm incididunt ut labore et dolore magna aliqua.
            </p><br>
            <span style="color: #11242c; text-transform: capitalize; font-weight: 400;">
              Fullstack developer
            </span>
          </div>
        </el-card>
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
      myProjectsText: `Here are a few recently projects that I have developed. If you have an idea or either a open source or private project don't doubt to contact me`,
      projects: [{}, {}, {}, {}]
    }
  }
}
</script>
<style scoped>
.my-projects {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-evenly;
  padding-top: 30px;
}

.card-whole {
  height: 180px;
  width: 90%;
  margin: 30px;
  border-bottom: 3px solid #42b883;
}
.body-project {
  padding: 30px;
}
</style>
