<template>
  <div>
    <h1>ชื่อผู้สมัครงาน : {{getFullname()}}</h1>
    <h1>อายุ : {{age}} ปี</h1>
    <h1><span v-html="address"></span></h1>
  </div>

</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      firstname: "chairat",
      lastname: "chaikong",
      age: 20, 
      address:"<strong>เชียงใหม่</strong>"
    }
  },
  methods:{
    getFullname() {
      return this.firstname + " " + this.lastname
    }
  }
}

</script>

<style>

</style>
