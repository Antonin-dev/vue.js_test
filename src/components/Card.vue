<template>
  <div>
    <div class="card" v-for="(task, index) in tasks" v-bind:key="index">
      <h2>{{ task.title }}</h2>
      <p>{{ task.content }}</p>
      <button v-on:click="deleteTask(index)">Supprimer</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: [
    "tasks"
  ],
  methods: {
    deleteTask(index) {
      this.tasks.splice(index, 1)
    }
  }
}
</script>

<style scoped>
.card{
  background-color: lightskyblue;
  width: 50%;
  margin: auto;
  padding: 10px;
  border-radius: 15px;
  margin-top: 15px;
}
</style>
