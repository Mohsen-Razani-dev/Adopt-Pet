<template>
  <div class="subForm">
    <el-form
      :model="ruleForm"
      :rules="rules"
      ref="ruleForm"
      label-width="120px"
      class="submitform"
    >
      <el-row class="submitformRow">
        <el-col :md="12" :sm="12" class="submitformCol">
          <el-input
            class="submitformInput"
            v-model="ruleForm.name"
            placeholder="Name"
            style="width: 100%;"
          ></el-input>
        </el-col>
        <el-col :md="12" :sm="12" class="submitformCol">
          <el-select
            v-model="ruleForm.gender"
            placeholder="Select"
            style="width: 100%;"
          >
            <el-option
              v-for="item in Gender"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </el-col>

        <el-col :md="12" :sm="12" class="submitformCol">
          <el-input
            v-model="ruleForm.email"
            placeholder="Email"
            style="width: 100%;"
          ></el-input>
        </el-col>

        <el-col :md="12" :sm="12" class="submitformCol">
          <el-input
            v-model="ruleForm.phone"
            placeholder="Phone"
            style="width: 100%;"
          ></el-input>
        </el-col>
        <el-col :md="12" :sm="12" class="submitformCol">
          <el-date-picker
            type="date"
            placeholder="Pick a date"
            v-model="ruleForm.date"
            style="width: 100%;"
          ></el-date-picker>
        </el-col>
        <el-col :md="12" :sm="12" class="submitformCol">
          <el-time-picker
            placeholder="Pick a time"
            v-model="ruleForm.time"
            style="width: 100%;"
          ></el-time-picker>
        </el-col>

        <el-col :md="12" :sm="12" class="submitformCol">
          <el-select
            v-model="ruleForm.problem"
            placeholder="Select"
            style="width: 100%;"
          >
            <el-option
              v-for="item in Problems"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
        </el-col>

        <el-col :md="12" :sm="12" class="submitformCol">
          <el-input
            v-model="ruleForm.weight"
            placeholder="Weight"
            style="width: 100%;"
          ></el-input>
        </el-col>

        <el-col :md="24" class="submitformCol">
          <el-input placeholder="Message" type="textarea" v-model="ruleForm.message" style="width: 100%;"></el-input>
        </el-col>

        <el-col :md="24" class="submitformCol">
          <button style="width: 100%;">Submit</button>
        </el-col>
      </el-row>
    </el-form>
  </div>
</template>

<script>
export default {
  name: 'Appointment',
  data() {
    return {
      ruleForm: {
        name: '',
        pass: '',
        gender: '',
        email: '',
        phone: '',
        date: '',
        time: '',
        problem: '',
        weight: '',
        message: '',
      },
      Gender: [
        {
          value: 'Male',
          label: 'Male',
        },
        {
          value: 'Female',
          label: 'Female',
        },
      ],
      Problems: [
        {
          value: 'checkup',
          label: 'checkup',
        },
        {
          value: 'eyes',
          label: 'eyes',
        },
        {
          value: 'skin',
          label: 'skin',
        },
        {
          value: 'heir',
          label: 'heir',
        },
        {
          value: 'emergency',
          label: 'emergency',
        },
      ],
    }
  },
}
</script>

<style lang="scss">
.subForm {
  border-radius: 5px;
  padding: 10px 10px 10px 10px;
  background-color: rgb(234, 241, 220);
  .submitform{
    .submitformRow{
      .submitformCol{
        padding: 7px;
        button{
          background-color: #aedc46;
          border: none;
          padding: 15px 0;
          color: white;
          font-size: 24px;
          width: 100%;
        }
        .submitformInput{
         height: auto;
        }
      }
    }
  }
}
</style>
