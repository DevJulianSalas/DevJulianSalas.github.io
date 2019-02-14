<template>
  <div>
    <SubHeader 
      subheader="my medium post"
      :subtext="myPostsText"
    />
    <el-row
      type="flex"
      class="my-posts"
    >
      <el-col 
        v-for="(item, index) in postmedium"
        :key="index"
        :span="9"
        style="width: 40%"
      >
        <el-card 
          :body-style="{ padding: '0px' }"
          class="card-whole"
          shadow="hover"
        >
          <img 
            src="https://lh3.googleusercontent.com/2HlOplHp25Z6-kQsbpfmMKWQzZ50dc5r2k1eZMxrsAG9fRB3F2D0YAYLQSXTWliJJd1OPsSI-5x1dBcAR7K42Mtd_TFHAWbuAjqakx7FUeH3VpYxqVc75aRZD7lV5I2UeIt-amqcYk9T54dWH_xI8IaZhnX2aDiZVxcZh6__vC6cOHaZ1rwB4zxbypug5z-0dMtH9bkVGcLHtxQCozod7gE9DVuzQj6_tT7Pzc_1hm-65fSHhmmJSFgkkgQtRkLvSVeDe-Uri-P6_r2ueoJFNeQxGzpAsP6b5gmp2hSQQORRoD2-2QZKyvJGfmTvf_P9yDMIYjOgyiOisTSsgkJuK-T-355TlzreyDwHguPHaBhrQxPMraNAB2-Oe7hr8Yz-f3-Ei_qEZroO7h1uVasErQoOwPzFavhtSVGdTXHajfz0ARiq0p_RLT7b27l3A37_NO3-c3HZR27rrkvz4CFrMT0oAt8IEVECJLdNZjivI7lfhVkxFB2r_vNPsCSK8NbtO35X36pX2ebpyi-H9rzxcPoMP8bze6RqPzj9b3APejiPtcFFi-u3405BgStP1OCvy3wFqAgnsBiGnfDwI0WE339H-XGk3_YTTaOzexkTJrJVOH1X2Flnj7Z7_A2rrrz8kN-LlY98eQcjLjUocxKPeYfd33zjWz0sLpWX9wjok4J5Cz2cOpvjhfDU8G3heFla08RTa2aFhmQU4s16Y8o0cvZU=w1117-h698-no" 
            class="image"
          >
          <div style="padding: 14px;">
            <div style="display: flex; flex-flow: row wrap; justify-content: center; align-items: center;">
              <span style="color: #11242c; font-size: 20px; text-transform: capitalize; font-weight: 500; flex: 1">
                {{ item.title }}
              </span>
              <a target='_blank' rel='noopener noreferrer' :href="item.link">see more</a>
            </div>
            <div>
              <p style="padding-top: 10px;">
                {{ item.description | stripHtml }}
              </p><br>
            </div>
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
  filters: {
    stripHtml: function(value) {
      const regex = /(<([^>]+)>)/gi
      const text = value.replace(regex, '')
      const shotText = text.slice(0, 150)
      return shotText + '...'
    }
  },
  props: {
    postmedium: {
      type: Array,
      required: true
    }
  },
  data: function() {
    return {
      myPostsText: `
      Nunc Placerat Mi Id Nisi Interdum Mollis. Scelerisque Mattis, Leo Quam Aliquet Diam, Congue Laoreet Elit Metus Eget Diam.`
    }
  }
}
</script>
<style scoped>
.my-posts {
  display: flex;
  flex-flow: row wrap;
  justify-content: space-evenly;
  padding-top: 30px;
}
.card-whole {
  height: 460px;
  width: 90%;
  margin: 30px;
}
.image {
  width: 100%;
  display: block;
}
a {
  font-size: 15px;
  color: #42b883;
  text-transform: capitalize;
  font-weight: 600;
}
</style>
