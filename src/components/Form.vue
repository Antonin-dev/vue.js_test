<template>
  <div>
    <h1>TodoList</h1>
    <form class="formulaire">
      <label for="title">Saisir le titre</label>
      <input type="text" id="title" name="title" v-model="title">
      <label for="content">Votre message</label>
      <input type="text" name="content" id="content" v-model="content">
      <button v-on:click.prevent="checkForm" value="valider">Valider</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "Form",
  data() {
    return {
      title: "",
      content: "",
      arrayTodo: []
    }
  },
  methods: {
    checkForm: function () {
      const task = {
        title: this.title,
        content: this.content
      }
      this.title = "";
      this.content = "";
      //Envoie de l'event pour recuperer les données
      this.$emit("addTask", task);
    }
  }
}
</script>

<style scoped>
.formulaire{
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  height: 200px;
}
</style>
