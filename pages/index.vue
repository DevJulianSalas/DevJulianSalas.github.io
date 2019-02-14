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
        <el-col :span="12">
          <h2>Hello, I'm Julian Salas</h2>
          <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quasi ipsam odio dolorum, hic beatae numquam natus animi minus quo voluptas saepe qui omnis aut eos, fugit, eaque illum illo debitis.</p>
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
  </div>
</template>
<script>
import axios from 'axios'
import Services from '../components/Services'
import Experience from '../components/Experience'
import MyProjects from '../components/Projects'
import Blog from '../components/Blog'
export default {
  components: {
    Services,
    Experience,
    MyProjects,
    Blog
  },
  async asyncData({ $axios }) {
    try {
      const mediumUrl = `
      https://api.rss2json.com/v1/api.json?rss_url=https%3A%2F%2Fmedium.com%2Ffeed%2F%40Medium`
      const { data, status } = await axios.get(mediumUrl)
      if (status === 200) {
        const items = data.items.slice(0, 4)
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
