<template>
  <div id="employee-form">
    <form>
      <label>Employee name</label>
      <input type="text" />
      <label>Employee Email</label>
      <input type="text" />
      <button>Add Employee</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "employee-form"
};
</script>

<style scoped>
label {
  color: #05386b;
}
form {
  margin-bottom: 2rem;
}
button {
  background-color: #379683;
}
</style>