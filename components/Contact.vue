<template>
  <div style="margin: 50px;">
    <SubHeader 
      subheader="get in touch"
      :subtext="myContactText"
    />
    <el-row 
      type="flex"
      class="form-contact"
    >
      <el-form
        ref="payload" 
        :model="payload" 
        :rules="rules2" 
        size="medium"
        style="width: 55%"
      >
        <el-col :span="12">
          <el-form-item
            style="width: 95%;"
            prop="name"
          >
            <el-input
              v-model="payload.name"
              placeholder="Name"
            />
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item
            style="width: 95%;"
            prop="email"
          >
            <el-input
              v-model="payload.email"
              placeholder="email"
            />
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item
            style="width: 95%;"
          >
            <el-input
              v-model="payload.tel"
              placeholder="phone"
            />
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item
            style="width: 95%;"
            prop="subject"
          >
            <el-input
              v-model="payload.subject"
              placeholder="subject"
            />
          </el-form-item>
        </el-col>
        <el-col :span="24">
          <el-form-item
            style="width: 97.5%;"
          >
            <el-input
              v-model="payload.body"
              placeholder="body"
              type="textarea" 
            />
          </el-form-item>
        </el-col>
        <el-col :span="23">
          <el-form-item
            style="display: flex; justify-content: flex-end;"
          >
            <el-button 
              @click="submitForm('payload')"
            >
              Submit
            </el-button>
          </el-form-item>
        </el-col>
      </el-form>
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
      myContactText: `Nunc Placerat Mi Id Nisi Interdum Mollis. Scelerisque Mattis, Leo Quam Aliquet Diam, Congue Laoreet Elit Metus Eget Diam.`,
      payload: {
        name: '',
        email: '',
        tel: '',
        subject: '',
        body: ''
      },
      rules2: {
        name: [
          {
            required: true,
            trigger: 'blur'
          }
        ],
        email: [
          {
            required: true,
            trigger: 'blur'
          }
        ],
        subject: [
          {
            required: true,
            trigger: 'blur'
          }
        ]
      }
    }
  },
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate(valid => {
        if (valid) {
          alert('submit!')
        } else {
          return false
        }
      })
    },
    resetForm(formName) {
      this.$refs[formName].resetFields()
    }
  }
}
</script>
<style scoped>
.form-contact {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  margin: 50px;
}
</style>
