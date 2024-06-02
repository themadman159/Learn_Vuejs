<template>
  <div>
    <div>
      <form action="" @submit.prevent="submitForm">
        <div>
          <label for="">ชื่อพนักงาน</label>
          <input type="text" class="border" v-model="employee.name" />
          <label for="">เงินเดือน</label>
          <input type="number" class="border" v-model="employee.salary" />
        </div>
        <div>
          <label for="">position</label>
          <select name="" id="" class="border" v-model="employee.position">
            <option value="frontend">frontend</option>
            <option value="backend">backend</option>
            <option value="fullstack">fullstack</option>
          </select>
        </div>
        <div>
            <p>เพศ</p>
            <input type="radio" value="ชาย" v-model="employee.gender">
            <label for="">ชาย</label>
            <input type="radio" value="หญิง" v-model="employee.gender">
            <label for="">หญิง</label>
        </div>
        <div>
            <p>ความสามารถพิเศษ</p>
            <input type="checkbox" name="" id="" value="ว่ายน้ำ" v-model="employee.hobbys">
            <label for="">ว่ายน้ำ</label>
            <input type="checkbox" name="" id="" value="เล่นดนตรี" v-model="employee.hobbys">
            <label for="">เล่นดนตรี</label>
            <input type="checkbox" name="" id="" value="เล่นเกม" v-model="employee.hobbys">
            <label for="">เล่นเกม</label>
            <input type="checkbox" name="" id="" value="นอน" v-model="employee.hobbys">
            <label for="">นอน</label>
        </div>
        <button type="submit">บันทึกข้อมูล</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "FormComponent",
  data() {
    return {
      employee: {
        name: "",
        salary: 0,
        position: "",
        gender: "",
        hobbys: [],
      },
    };
  },
  methods:{
    submitForm(){
        const newEmployee = {
            name: this.employee.name,
            salary: this.employee.salary,
            position: this.employee.position,
            gender: this.employee.gender,
            hobbys: this.employee.hobbys
        }
        this.$emit("employeeSumbit",newEmployee)
        this.resetForm()
    },
    resetForm(){
        this.employee.name = "",
        this.employee.salary = 0,
        this.employee.position = "",
        this.employee.gender = "",
        this.employee.hobbys = []
    }
  }
};
</script>   

<style>
</style>