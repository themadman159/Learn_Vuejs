<template>
    <div>
        <ul>
            <PersonData
                v-for="(person, index) in employees"
                :key="index"
                :name="person.name"
                :salary="person.salary"
                :position="person.position"
                :gender="person.gender"
                :hobbys="person.hobbys"
            />
        </ul>
    </div>
</template>

<script>
import PersonData from "./PersonData.vue";
export default {
    name: "ListData",
    components: {
        PersonData,
    },
    props:["employees"]
};
</script>

<style>
</style>
