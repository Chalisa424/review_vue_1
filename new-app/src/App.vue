<template>
  <div>
    <div>
      <div>First Name</div>
      <input type="text" name="firstname" v-model="formData.firstname" />
    </div>
    <div>
      <div>Last Name</div>
      <input type="text" name="lastname" v-model="formData.lastname" />
    </div>
    <div>
      <div>Genger</div>
      <div v-for="gender in genderList">
        <input type="radio" name="gender" :value="gender" v-model="formData.gender" />
        {{ gender }}
      </div>
    </div>
    <div>
      <div>Interest</div>
      <div v-for="interest in interestList">
        <input type="checkbox" name="interest" :value="interest" v-model="formData.interest"/>
        {{ interest }}
      </div>
    </div>
    <div>
      <div>Description</div>
      <textarea name="description" v-model="formData.description" ></textarea>
    </div>
    <button @click="submitForm()">Submit</button>
  </div>
</template>

<script setup>
import { reactive } from 'vue';

const genderList = ["ผู้ชาย", "ผู้หญิง", "ไม่ระบุเพศ"];
const interestList = ["เกม", "กีฬา", "การเมือง", "ฟังเพลง"];

const formData = reactive({
  interest:[]
})

const submitForm = () =>{
  console.log('submit')
  console.log('formdata', formData)
  console.log('interest',formData.interest.join())
}
</script>
