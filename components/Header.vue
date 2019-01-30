<template>
  <div>
    <el-row justify="center" type="flex" style="margin: 10px;">
      <el-col :span="24">
        <p>logo</p>
      </el-col>
    </el-row>
    <div class="group-message-me">
      <el-row justify="center" type="flex" style="margin: 10px;" align="bottom">
      <el-col class="message-front" :span="24">
        I am Julian Salas <span style="color:#f95231">
          .
        </span>
      </el-col>
    </el-row>
    <el-row justify="center" type="flex">
      <el-col class="message-me" :span="15">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Distinctio rem in repudiandae. Repellendus sint rem error dolorem tenetur, iste aliquid ipsam quam. Provident deleniti in quo architecto ea, nemo qui.</p>
      </el-col>
    </el-row>  
    </div>
  </div>
</template>
<script>
export default {}
</script>
<style scoped>
.group-message-me {
  position: absolute;
  top: 30%;
}
.message-front {
  font-family: 'Poppins', sans-serif;
  font-size: 40px;
  font-weight: 700;
  color: #11242c;
  line-height: 1.8em;
  text-align: center;
  margin: 0;
  width: 100%;
}

.message-me p {
  font-family: 'Poppins', sans-serif;
  font-size: 22px;
  color: #203b4c;
  font-weight: 300;
  line-height: 1.5em;
  text-align: center;
  margin: 0;
  width: 100%;
}
</style>
