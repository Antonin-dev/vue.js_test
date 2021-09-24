<template>
  <div id="app">
    <Form @addTask="onAddTask"/>
    <Card :tasks="tasks"/>
  </div>
</template>

<script>
import Form from "@/components/Form";
import Card from "@/components/Card";


export default {
  name: 'App',
  components: {
    Form,
    Card
  },
  data(){
    return {
      tasks: [
      ]
    }
  },
  methods: {
    onAddTask: function(task) {
      this.tasks.push(task);
    }
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
