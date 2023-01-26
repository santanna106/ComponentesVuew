<template>
  <div>
    <Pessoa />
    <SimpleComponent />
  </div>
</template>
<script>
import { defineComponent } from '@vue/composition-api'
import Pessoa from './components/Pessoa.vue';
import SimpleComponent from './components/SimpleComponent.vue';

export default defineComponent({
  name:'App',
  components: {
    Pessoa,
    SimpleComponent
  },
  setup() {
    
  },
})
</script>
