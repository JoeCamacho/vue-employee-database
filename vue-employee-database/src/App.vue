<template>
  <div id="app">
    <h1>Employees</h1>
    <employee-table />
  </div>
</template>

<script>
import EmployeeTable from "@/components/EmployeeTable.vue";
export default {
  name: "app",
  components: {
    EmployeeTable
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
