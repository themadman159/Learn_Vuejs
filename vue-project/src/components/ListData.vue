<template>
    <div>
        <ul>
            <PersonData
                v-for="(person, index) in employees"
                :key="index"
                :id="person.id"
                :name="person.name"
                :salary="person.salary"
                :position="person.position"
                :showData="person.showData"
                @show="toggleShowData"
                @delete="deletePerson"
            />
        </ul>
    </div>
</template>

<script>
import PersonData from "./PersonData.vue";
export default {
    name: "ListData",
    data() {
        return {
            employees: [
                { id: 1, name: "mr.A", salary: 20000, position: "fullstack", showData: false },
                { id: 2, name: "mr.B", salary: 20000, position: "frontend", showData: false },
                { id: 3, name: "mr.C", salary: 20000, position: "backend", showData: false },
                { id: 4, name: "mr.D", salary: 20000, position: "QA", showData: false },
            ],
        };
    },
    components: {
        PersonData,
    },
    methods: {
        toggleShowData(employee_id) {
            this.employees = this.employees.map(employee => {
                if (employee.id === employee_id) {
                    return { ...employee, showData: !employee.showData };
                }
                return employee;
            });
        },
        deletePerson(employee_id) {
            this.employees = this.employees.filter(employee => {
                return employee.id !== employee_id
            })
        }
    },
};
</script>

<style>
</style>
