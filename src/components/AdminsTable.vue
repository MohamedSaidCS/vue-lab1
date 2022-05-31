<template>
  <h1>Admins</h1>
  <table>
    <thead>
    <tr>
      <th>Name</th>
      <th>Age</th>
      <th>Address</th>
      <th>Action</th>
    </tr>
    </thead>
    <tbody>
    <tr v-for="(student,index) in admins" :key="index">
      <td>{{ student.name }}</td>
      <td>{{ student.age }}</td>
      <td>{{ student.address }}</td>
      <td>
        <button @click="$emit('delete', {type: 'admin', index: index})">Delete</button>
      </td>
    </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  name: "AdminsTable",
  emits: ['delete'],
  props: {
    admins: Array
  },
}
</script>

<style scoped>

</style>
