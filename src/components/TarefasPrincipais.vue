<template>
    <div class="box has-text-weight-bold">
        <div class="columns">
            <div class="column is-7">
                Descrição
            </div>
            <div class="column">
                <CronometroPrincipal :tempoEmSegundos="15"/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CronometroPrincipal from './CronometroPrincipal.vue'


export default defineComponent({
    name : 'TarefasPrincipais',

    components : {
        CronometroPrincipal,
    }
})
</script>

<style scoped>

.box{
    background-color: #FAF0CA;
}
</style>