<template>
     <p>TESTE {{nome}}</p>
</template>
<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
    name:'Pessoa',
    data(){
        return{
            nome: 'Gabriel'
        }
    }
})
</script>
