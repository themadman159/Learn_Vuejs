<template>
    <CustomCard>
        <template v-slot:header-Card>
            <p>ชื่อ: {{ name }}</p>
        </template>
        <template v-slot:content-Card>
                <p>เงินเดือน : {{ salary }}</p>
                <p>ตำแหน่ง : {{ position }}</p>
                {{ showData }}
                <p>เพศ : {{gender}}</p>
                <p>ความสามารถพิเศษความสามารถพิเศษ : {{hobbys}}</p>
        </template>
    </CustomCard>
</template>

<script>
import CustomCard from "./CustomCard.vue";
export default {
  name: "PersonData",
  data() {
    return {};
  },
  components: {
    CustomCard,
  },
  props: {
    id: {
      type: Number,
    },
    name: {
      type: String,
      required: true,
    },
    salary: {
      type: Number,
      required: true,
    },
    position: {
      type: String,
      required: true,
    },
    gender:{
        type: String,
        required: true,
    },
    hobbys:{
        type: Array,
        required: true,
    }
  },
};
</script>

<style>
</style>