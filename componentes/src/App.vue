<template>
  <div id="app">
    <TodoForm @addTarefa="adicionarTarefa($event)"/>
    <TodoList :tarefas="tarefas"/>
  </div>
</template>

<script>
import TodoForm from "./components/TodoForm.vue"
import TodoList from "./components/TodoList.vue"

export default {
  name: 'App',
  components: {
    TodoForm, TodoList
  }, data:function(){
    return{
        tarefas:[
        {descricao:"Matemática"},
        {descricao:"Biologia"},
        {descricao:"Geografia"},
      ]
    }
  },
  methods:{
    adicionarTarefa: function(event){
      this.tarefas.push({descricao: event.novaTarefa})
    }
   }
}
</script>

<style>
</style>
