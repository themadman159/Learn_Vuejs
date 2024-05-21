<template>
    <div>
        <p>ชื่อ: {{name}} เงินเดือน : {{salary}} ตำแหน่ง : {{position}}</p>
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
        }
    }
};
</script>

<style>
</style>