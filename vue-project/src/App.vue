<template>
  <div>
    <h1>Root component</h1>
    <ListData :employee="employee" />
    <FormComponent />
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
  data() {
    return {
      employee: [
        { name: "mr.A", salary: 20000, position: "fullstack" },
        { name: "mr.B", salary: 20000, position: "frontend" },
        { name: "mr.C", salary: 20000, position: "backend" },
        { name: "mr.D", salary: 20000, position: "QA" },
      ],
    };
  },
};
</script>

<style>
</style>
