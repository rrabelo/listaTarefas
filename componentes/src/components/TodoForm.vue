<template>
    <div id="adicionar">    
        <div class="form">
            <input type="text" placeholder="Adicionar Tarefa" v-model="titulo"/>
            <button @click="adicionar">add</button>
        </div>
    </div>
  
</template>

<script>
export default {
    name: "TodoForm",
    props: [tarefas],
    data: function() {
        return {
            titulo: "",
            cor: "background: gree"
        }
    }, 
    methods:{
        adicionar: function(){
            this.$emit("AdicionarTexto", {
                titulo: this.titulo,
                cor: this.cor
            })
        }
    }

}
</script>

<style>

#adicionar {
    width: 600px;
    height: 50px;
    border: 1px solid #fff;
    margin: 30 px auto 0 auto;
}

.form input {
    margin: 8px 0 10px 10px;
    user-select: none;
    border: none;
    width: 300px;
    height: 30px;
    font-size: 17px ;
}

.form button{
    margin-left: 140px;
    border: none;
    border-radius: 2px;
    width: 100px;
    height: 30px;
    cursor: pointer;

}



</style>