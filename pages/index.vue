<template>
  <div>
    <section class="container">
      <el-row type="flex" class="about-us">
        <el-col :span="11">
          <img 
            src="../assets/image/me3.jpeg" 
            alt="here go me"
            class="me"
          >
        </el-col>
        <el-col :span="12" style="padding-top:80px;">
          <h2>Hello, I'm Julian Salas</h2>
          <div class="text-info">
            I'm a confident, curious, adventurous and receptive person who take risks and assume his fails with humbly. I think that success and learning come from failure after failure. I enjoy spending time with my family, especially these small moments that make life easy. I love swinging, take a cup of coffee in the mornings, reading and watch Netflix. <br/><br/>
            I am a persistence, recursive, focused and reliable person that works hard to achieve all set goals successfully. I like working alone as well as in a team situation; I am convinced that collective knowledge can bring big things.
          </div>
          <div style="padding-top: 20px; padding-bottom: 20px;">
            <Networks />
          </div>
          <el-row type="flex">
            <el-col :span="6">
              <el-button 
                plain
                size="large"
                style=""
              >
                Hire me
              </el-button>
            </el-col>
            <el-col :span="6">
              <el-button plain>
                Download CV
              </el-button>
            </el-col>
          </el-row>
        </el-col>
      </el-row>
    </section>
    <Services />
    <Experience />
    <MyProjects />
    <Blog 
      :postmedium="postMedium" 
    />
    <Contact />
  </div>
</template>
<script>
import axios from 'axios'
import Services from '../components/Services'
import Experience from '../components/Experience'
import MyProjects from '../components/Projects'
import Blog from '../components/Blog'
import Contact from '../components/Contact'
import Networks from '../components/Networks'
export default {
  components: {
    Services,
    Experience,
    MyProjects,
    Blog,
    Contact,
    Networks
  },
  async asyncData({ $axios }) {
    try {
      const mediumUrl = `
      https://api.rss2json.com/v1/api.json?rss_url=https%3A%2F%2Fmedium.com%2Ffeed%2F%40Medium`
      const { data, status } = await axios.get(mediumUrl)
      if (status === 200) {
        const items = data.items.slice(0, 3)
        return {
          postMedium: items
        }
      }
    } catch (error) {
      throw new Error(error)
    }
  },
  data: function() {
    return {
      postMedium: []
    }
  }
}
</script>

<style>
p {
  margin: 0 0 10px;
  text-transform: capitalize;
  color: #555;
  font-size: 14px;
  font-weight: 500;
}

.text-info {
  margin: 0 0 10px;
  color: #555;
  line-height: 24px;
  font-size: 14px;
  font-weight: 500;
  padding-top: 10px;
}

.about-us {
  margin: 15%;
}

.me {
  width: 80%;
  max-width: 100%;
}
.subtext {
  font-size: 14px;
  line-height: 34px;
  text-transform: capitalize;
  color: #555;
  font-size: 14px;
  font-weight: 548;
}
</style>
