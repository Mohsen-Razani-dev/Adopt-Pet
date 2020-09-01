<template>
  <div class="mainform">
    <el-form
      :model="ruleForm"
      :rules="rules"
      ref="ruleForm"
      label-width="120px"
      label-position="top"
      class="HomepaeForm"
    >
      <el-form-item class="label" label="Full name" prop="name">
        <el-input
          v-model="ruleForm.name"
          placeholder="ex : Mohsen Razani"
        ></el-input>
      </el-form-item>
      <el-form-item class="label" prop="email" label="Email">
        <el-input
          v-model="ruleForm.email"
          placeholder="ex : Mohsenrazani.z@gmail.com"
        ></el-input>
      </el-form-item>
      <el-form-item class="label" label="Password" prop="pass">
        <el-input
          type="password"
          v-model="ruleForm.pass"
          autocomplete="off"
          show-password
        ></el-input>
      </el-form-item>
      <el-form-item class="label" label="Gender" prop="gender">
        <el-radio-group
          v-model="ruleForm.gender"
          style="display: flex !important;"
        >
          <el-radio label="Female"></el-radio>
          <el-radio label="Male"></el-radio>
          <el-radio label="Other"></el-radio>
        </el-radio-group>
      </el-form-item>
      <el-form-item class="signupbtns">
        <el-button
          class="createbtn"
          type="success"
          @click="submitForm('ruleForm')"
          plain
          round
          >Create</el-button
        >
        <div class="login">
          <p>i already have an account</p>
          <a href="#">login</a>
        </div>
      </el-form-item>
      <el-form-item class="label" prop="type">
        <el-checkbox-group
          style="display: flex !important;"
          v-model="ruleForm.type"
        >
          <el-checkbox
            label="i accept the terms of use and privacy policy"
            name="type"
          ></el-checkbox>
        </el-checkbox-group>
      </el-form-item>
    </el-form>
  </div>
</template>
<script>
export default {
  name: 'HomepageJoin',
  data() {
    return {
      ruleForm: {
        name: '',
        pass: '',
        delivery: false,
        type: [],
        gender: '',
        email: '',
      },
      rules: {
        gender: [
          {
            required: true,
            message: 'Please choice your Gender',
            trigger: 'blur',
          },
        ],
        pass: [
          {
            required: true,
            message: 'Please input Password',
            trigger: 'blur',
          },
          {
            min: 6,
            max: 12,
            message: 'Length should be 6 to 12',
            trigger: 'blur',
          },
        ],
        name: [
          {
            required: true,
            message: 'Please input Activity name',
            trigger: 'blur',
          },
          {
            min: 3,
            max: 30,
            message: 'Length should be 3 to 5',
            trigger: 'blur',
          },
        ],
        type: [
          {
            type: 'array',
            required: true,
            message: 'Please select at least one activity type',
            trigger: 'change',
          },
        ],
        resource: [
          {
            required: true,
            message: 'Please select activity resource',
            trigger: 'change',
          },
        ],
        email: [
          {
            required: true,
            message: 'Please input email address',
            trigger: 'blur',
          },
          {
            type: 'email',
            message: 'Please input correct email address',
            trigger: ['blur', 'change'],
          },
        ],
      },
    }
  },
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate((valid) => {
        if (valid) {
          alert('submit!')
        } else {
          console.log('error submit!!')
          return false
        }
      })
    },
    resetForm(formName) {
      this.$refs[formName].resetFields()
    },
  },
}
</script>
<style lang="scss">
.mainform {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  .HomepaeForm {
    width: 100%;
    .label {
      label {
        padding: 0 !important;
        line-height: 30px !important;
        font-size: 13px !important;
        display: inline !important;
      }
    }
    .signupbtns {
      padding: 5px 0 0 0;
      .createbtn {
        width: 100%;
      }
      .login {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 10px;
        p {
          margin-right: 10px;
          font-size: 16px;
        }
        a {
          color: #6f608c;
          text-decoration: none;
          font-size: 16px;
        }
      }
    }
  }
}
.el-radio__inner:hover {
  outline: none;
  border: none;
}
.el-radio__input.is-checked .el-radio__inner {
  background: #82ce5c;
  border: 1px solid #82ce5c;
  outline: none;
}
.el-radio__input.is-checked + .el-radio__label {
  color: #82ce5c;
  outline: none;
}
.el-checkbox__input.is-checked .el-checkbox__inner,
.el-checkbox__input.is-indeterminate .el-checkbox__inner {
  background: #82ce5c;
  border: 1px solid #82ce5c;
  outline: none;
}
.el-checkbox__input.is-checked .el-checkbox__inner,
.el-checkbox__input.is-indeterminate .el-checkbox__inner {
  background: #82ce5c;
  border: 1px solid #82ce5c;
  outline: none;
}
.el-checkbox__input.is-focus .el-checkbox__inner {
  border: 1px solid #82ce5c;
  outline: none;
}
.el-checkbox__inner:hover {
  outline: none !important;
  border: none !important;
}
.el-checkbox__input.is-checked+.el-checkbox__label{
  color: #82ce5c;
  outline: none;
}
.el-checkbox__label{
  font-size: 11px;
}
.el-input__inner{
  border: 1px solid #82ce5c;
}
.el-input.is-active .el-input__inner, .el-input__inner:focus{
  border: 1px solid #3d801d;
}
</style>
