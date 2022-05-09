<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
      <BarraLateral />
    </div>
    <div class="column is-three-quarter">
      <FormularioPrincipal @aoSalvarTarefa="salvarTarefa"/>
      <div class="lista">
        <TarefasPrincipais v-for="(tarefa, index) in tarefas" :key="index" :tarefa="tarefa"/>
      </div>
    </div>

  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BarraLateral from './components/BarraLateral.vue';
import FormularioPrincipal from './components/FormularioPrincipal.vue';
import TarefasPrincipais from './components/TarefasPrincipais.vue';
import ITarefa from './interfaces/ITarefa'

export default defineComponent({
 name: 'App',
 components:{
   BarraLateral,
   FormularioPrincipal,
   TarefasPrincipais,
 } ,

data(){
  return{
    tarefas:[] as ITarefa[]
  }
}, 

methods: {
  salvarTarefa (tarefa: ITarefa){
    this.tarefas.push(tarefa)
  }
}

});

</script>

<style>

.lista{
  padding: 1.25rem;
}

</style>
