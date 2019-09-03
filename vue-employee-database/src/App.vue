<template>
  <div id="app" class="small-container">
    <h1>Employees</h1>
    <employee-form @add:employee="addEmployee" />
    <employee-table :employees="employees" />
  </div>
</template>

<script>
import EmployeeTable from "@/components/EmployeeTable.vue";
import EmployeeForm from "@/components/EmployeeForm.vue";
export default {
  name: "app",
  components: {
    EmployeeTable,
    EmployeeForm
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: "Kim Obasogie",
          email: "k.obasogie@gmail.com"
        },
        {
          id: 2,
          name: "Julie Pladys",
          email: "j.pladys@gmail.com"
        },
        {
          id: 3,
          name: "Lynn Brants",
          email: "l.brants@gmail.com"
        }
      ]
    };
  },
  methods: {
    addEmployee(employee) {
      const lastId =
        this.employees.length > 0
          ? this.employees[this.employees.length - 1].id
          : 0;
      const id = lastId + 1;
      const newEmployee = { ...employee, id };

      this.employees = [...this.employees, newEmployee];
    }
  }
};
</script>

<style scoped>
h1 {
  color: #05386b;
}
button {
  background: #5cdb95;
  border: 1px solid #5cdb95;
}

.small-container {
  max-width: 680px;
}
</style>
