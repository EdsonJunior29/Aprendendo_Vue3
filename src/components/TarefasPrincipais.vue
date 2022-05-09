<template>
    <div class="box has-text-weight-bold">
        <div class="columns">
            <div class="column is-7">{{ tarefa.descricao || 'Tarefa sem descrição' }}</div>
            <div class="column">
                <CronometroPrincipal :tempoEmSegundos="tarefa.duracaoEmSegundos"/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">

import { defineComponent , PropType} from 'vue'
import CronometroPrincipal from './CronometroPrincipal.vue'
import ITarefa from '../interfaces/ITarefa'

export default defineComponent({
    name : 'TarefasPrincipais',

 components : {
        CronometroPrincipal,
    },

    props: {
        tarefa: {
            type: Object as PropType<ITarefa>,
            requered: true
        }
    }

    
});
</script>

<style scoped>

.box{
    background-color: #FAF0CA;
}
</style>