<template>
  <div id="app">
    <todo-form :tarefas="tarefas" @AdicionarTexto="Adicionar($event)"/>
    <todo-list :tarefas="tarefas"/>
    
  </div>
</template>

<script>
import TodoForm from "./components/TodoForm.vue"
import TodoList from "./components/TodoList.vue"

export default {
  name: 'App',
  components: {
    TodoForm,
    TodoList
  },
  data: function(){
    return {
      tarefas: [
        {
          texto: "limpar a casa",
          cor: "background: green"
        }, {
          texto: "estudar alemão",
          cor: "background: blue"
        }, {
          texto: "estudar tecnico",
          cor: "background: red"
        }
      ]
    }
  }, methods: {
    Adicionar: function(event){
      this.tarefas.push({
        texto: event.titulo,
        cor: event.cor
      })
    }
  }
}
</script>

<style>

</style>
