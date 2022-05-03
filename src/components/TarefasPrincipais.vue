<template>
    <div class="box has-text-weight-bold">
        <div class="columns">
            <div class="column is-7">{{tarefa.descricao}}</div>
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
        terefa: {
            type: Object as PropType<ITarefa>,
        }
    }

    
});
</script>

<style scoped>

.box{
    background-color: #FAF0CA;
}
</style>