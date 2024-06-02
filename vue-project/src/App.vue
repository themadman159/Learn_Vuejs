<template>
  <div>
    <h1>Root component</h1>
    <div>
      <FormComponent @employeeSumbit="insertEmployee"/>
    </div>
    <div v-if="employees.length>0">
      <p>ข้อมูลพนักงาน</p>
      <ListData :employees="employees"/>
    </div>
    <div v-else>
      <p>ไม่มีข้อมูลพนักงาน</p>
    </div>
  </div>
</template>

<script>
import FormComponent from "./components/FormComponent.vue";
import ListData from "./components/ListData.vue";
export default {
  name: "App",
  components: {
    ListData,
    FormComponent,
  },
  data(){
    return{
      employees: []
    }
  },
  methods:{
    insertEmployee(employee){
      this.employees.push(employee);
    }
  }
};
</script>

<style>
</style>
