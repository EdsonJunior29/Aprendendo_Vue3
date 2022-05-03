<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
      <BarraLateral />
    </div>
    <div class="column is-three-quarter">
      <FormularioPrincipal/>
      <div class="lista">
        <TarefasPrincipais />
      </div>
    </div>

  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BarraLateral from './components/BarraLateral.vue';
import FormularioPrincipal from './components/FormularioPrincipal.vue';
import TarefasPrincipais from './components/TarefasPrincipais.vue';

export default defineComponent({
 name: 'App',
 components:{
   BarraLateral,
   FormularioPrincipal,
   TarefasPrincipais,
 }
});

</script>

<style>

.lista{
  padding: 1.25rem;
}

</style>
