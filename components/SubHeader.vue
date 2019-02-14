<template>
  <el-row
    type="flex"
    justify="center"
    class="subheader"
  >
    <el-col 
      :span="24"
      style="text-align: center;"
    >
      <h2>
        {{ subheader }} <span style="color:#f95231">
          .
        </span>
      </h2>
    </el-col>
    <el-col 
      :span="16"
      style="padding-top:5px;"
    >
      <p>{{ subtext }}</p>
    </el-col>
  </el-row>    
</template>
<script>
export default {
  props: {
    subheader: {
      required: true,
      type: String
    },
    subtext: {
      required: true,
      type: String,
      default: ''
    }
  }
}
</script>
<style scoped>
.subheader {
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
