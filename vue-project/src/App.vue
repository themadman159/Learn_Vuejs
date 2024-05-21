<template>
  <div>
    <h1>Root component</h1>
    <ListData :employee="employee" />
  </div>
</template>

<script>
import ListData from "./components/ListData.vue";
export default {
  name: "App",
  components: {
    ListData,
  },
  data() {
    return {
    };
  },
};
</script>

<style>
</style>
