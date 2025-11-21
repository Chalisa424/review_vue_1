<template>
  <div>
    <div>
      <div>First Name</div>
      <input type="text" name="firstname" />
    </div>
    <div>
      <div>Last Name</div>
      <input type="text" name="lastname" />
    </div>
    <div>
      <div>Gender</div>
      <div v-for="gender in genderList">
        <input type="radio" name="gender" :value="gender" />
        {{ gender }}
      </div>
    </div>
    <div>
      <div>Interest</div>
      <div v-for="interest in interestList">
        <input type="checkbox" name="interest" :value="interest" />
        {{ interest }}
      </div>
    </div>
    <div>
      <div>Description</div>
      <textarea name="description"></textarea>
    </div>
    <button @click="submitForm()">Submit</button>
  </div>
</template>
<script setup>
const genderList = ["ผู้ชาย", "ผู้หญิง", "ไม่ระบุเพศ"];
const interestList = ["กีฬา", "ดูหนัง", "ฟังเพลง", "ไปเที่ยว"];

const submitForm = () =>{
  console.log('submit')
}

</script>
