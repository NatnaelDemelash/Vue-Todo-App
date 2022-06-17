<template>
  <header>
    <h1>Task Tracker</h1>
    <Button @btn-click = "$emit('toggle-add-task')"  :title=" showAddTask ? 'Close' : 'AddTask'" :color=" showAddTask ?'red' : 'green'" />
  </header>
  <Tasks :tasks="tasks" />
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "Header",
  components: {
    Button,
  },
  props:{
    showAddTask: Boolean
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
