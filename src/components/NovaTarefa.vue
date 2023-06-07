<template>
    <NewBox> 
        <div class="columns">
            <div class="column is-7">{{tarefa.descricao || 'Tarefa sem descrição'}}</div>
            <div class="column">
                <Cronometro :tempoEmSegundos="tarefa.duracaoEmSegundos"/>
            </div>
        </div>
    </NewBox>   
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import Cronometro from './Cronometro.vue';
import ITarefa from '@/interfaces/ITarefa'
import NewBox from './NewBox.vue'


export default defineComponent({
    name: 'NovaTarefa',
    components: {
        Cronometro,
        NewBox
    },
    props: {
        tarefa: {
            type: Object as PropType<ITarefa>,
            required: true    
        }
    }
});        
</script>

