<template>
  <div id="lista">
      <div class="tarefas" v-for="(tarefa, index) in tarefas" :key="index" :style="tarefa.cor">
            {{tarefa.texto}}
      </div>
  </div>
</template>

<script>
export default {
    name: "lista",
    props: ['tarefas']
}
</script>

<style>
    #lista{
        color: #fff;
        display: flex;
        width: 800px;
        height: 200px;
        border: 1px solid #fff;
        margin: 50px auto 0 auto;
        flex-wrap: wrap;
    }

    .tarefa{
        width: 150px;
        height: 30px;
        border: 1px solid #fff;
        margin: 10px 0 0 10px;
        text-align: center;
        line-height: 30px;
        user-select: none;
        cursor: pointer;
    }


</style>