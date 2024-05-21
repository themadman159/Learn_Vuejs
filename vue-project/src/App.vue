<template>
  <div>
    <img v-bind:src="picture" alt="" />
    <h1>ชื่อผู้สมัครงาน : {{ getFullname() }}</h1>
    <h1>อายุ : {{ age }} ปี</h1>
    <form @submit.prevent="submitForm">
      <label for="">กรอกชื่อเล่น</label>
      <input type="text" @input="setNickname">
      <button type="submit">บันทึกชื่อเล่น</button>
    </form>
    <h1>ชื่อเล่น : {{nickname}}</h1>
    <h1><span v-html="address"></span></h1>
    
    <h1>งานอดิเรก</h1>
    <ul>
      <li>{{ hobby[0] }}</li>
      <li>{{ hobby[1] }}</li>
      <li>{{ hobby[2] }}</li>
    </ul>
    <h1>ข้อมูล</h1>
    <ul>
      <li>{{ general.gender }}</li>
      <li>{{ general.height }}</li>
      <li>{{ general.weight }}</li>
      <li>{{ general.status }}</li>
    </ul>
    <button @click.left="showData">คลิกเพื่อดูข้อมูล</button>
    <button @click.left="increment">increment</button>
    <button @click.left="decrement">decrement</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstname: "chairat",
      nickname:"",
      lastname: "chaikong",
      age: 20,
      address: "<strong>เชียงใหม่</strong>",
      picture:
        "https://icons.iconarchive.com/icons/justicon/free-simple-line/256/Website-Browser-Layout-Interface-icon.png",
      social: "www.facebook.com",
      hobby: ["เล่นเกม", "ฟังเพลง", "นอน"],
      general: {
        gender: "male",
        height: 163,
        weight: 55,
        status: true,
      },
    };
  },
  methods: {
    getFullname() {
      return this.firstname + " " + this.lastname;
    },
    showData() {
      alert(this.firstname + " " + this.lastname);
    },
    increment() {
      this.age++;
    },
    decrement() {
      this.age--;
      if (this.age <= 0) {
        this.age = 0;
      }
    },
    setNickname(e){
      this.nickname = e.target.value;
    },
    submitForm(){
      alert("บันทึกชื่อเล่นเรียบร้อย")
    }
  },
};
</script>

<style>
</style>
