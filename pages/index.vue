<template>
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
      <el-col :span="6">
        <p>s</p>
      </el-col>
      
    </el-row>
    
    <p>Esto es la page principal</p>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
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
</style>
