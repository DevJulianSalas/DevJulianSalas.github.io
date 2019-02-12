<template>
  <div>
    <el-row
      type="flex"
      justify="center"
      class="services"
    >
      <el-col 
        :span="24"
        style="text-align: center;"
      >
        <h2>
          what I love to do <span style="color:#f95231">
            .
          </span>
        </h2>
      </el-col>
      <el-col 
        :span="16"
        style="padding-top:5px;"
      >
        <p>Nunc Placerat Mi Id Nisi Interdum Mollis. Scelerisque Mattis, Leo Quam Aliquet Diam, Congue Laoreet Elit Metus Eget Diam.</p>
      </el-col>
    </el-row>
    <el-row
      type="flex"
      justify="center"
      style="flex-flow: row wrap; margin: 60px; padding-top:20px;"
    >
      <el-col
        v-for="(item, index) in services"
        :key="index"
        :span="8"
        style="text-align: center;"
      >
        <div>
          <span>{{item.name}}</span>
          <span>{{item.icon}}</span>
        </div>
        <p>{{item.description}}</p>
      </el-col>
    </el-row>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      services: [
        {
          name: 'Branding',
          description: `Fringilla augue at maximus vesti Nam pulvinar vitae neque etrolling freight.`,
          icon: 'text'
        },
        {
          name: 'Branding',
          description: `Fringilla augue at maximus vesti Nam pulvinar vitae neque etrolling freight.`,
          icon: 'text'
        },
        {
          name: 'Branding',
          description: `Fringilla augue at maximus vesti Nam pulvinar vitae neque etrolling freight.`,
          icon: 'text'
        },
        {
          name: 'Branding',
          description: `Fringilla augue at maximus vesti Nam pulvinar vitae neque etrolling freight.`,
          icon: 'text'
        },
        {
          name: 'Branding',
          description: `Fringilla augue at maximus vesti Nam pulvinar vitae neque etrolling freight.`,
          icon: 'text'
        },
        {
          name: 'Branding',
          description: `Fringilla augue at maximus vesti Nam pulvinar vitae neque etrolling freight.`,
          icon: 'text'
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
