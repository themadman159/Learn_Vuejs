<template>
    <div>
        <ul>
            <PersonData v-for="(person,index) in employee" 
            :key="index" 
            :name="person.name" 
            :salary="person.salary" 
            :position="person.position"
            />
        </ul>
    </div>
</template>

<script>
import PersonData from './PersonData.vue'
export default {
    name: "ListData",
    data(){
        return{
            msg: "แสดงรายชื่อพนักงาน"
        }        
    },
    components:{
        PersonData
    },
    props:["employee"]
}
</script>

<style>

</style>