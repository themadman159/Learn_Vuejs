<template>
    <div>
        <p>ชื่อ: {{name}}</p>
        <div v-show="showData">
            <p>เงินเดือน : {{salary}}</p>
            <p>ตำแหน่ง : {{position}}</p>
        </div>
        <button class="border" @click="showPersonData(id)">ดูข้อมูล</button>
        <button class="border" @click="deletePerson(id)">ลบข้อมูล</button>
        {{showData}}
    </div>
</template>

<script>
export default {
    name: "PersonData",
    data() {
        return {
        };
    },
    props:{
        id:{
            type:Number
        },
        name:{
            type:String,
            required:true
        },
        salary:{
            type:Number,
            required:true
        },
        position:{
            type:String,
            required:true
        },
        showData:{
            type:Boolean,
            required:true
        }
    },
    methods:{
        showPersonData(id){
            this.$emit("show",id)
        },
        deletePerson(id){
            this.$emit("delete",id)
        }
    }
};
</script>

<style>
</style>