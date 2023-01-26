<template>
  <p>All of your components html goes inside these template tags {{msg}}</p>
  <t-input
      bg="bg-gray-200"
      autocomplete="on"
      id="email"
      name="email"
      v-model="user.email"
      label="Email"
      type="email"
      error="errores we"
    ></t-input>
</template>
<script>
  import { defineComponent } from '@vue/composition-api';
  import TInput from "./t-input.vue";

  export default defineComponent({
    name: "simple-component",
    components: {
      TInput
    },
    data() {
      return {
        msg: "My Profile Component",
        user: {
          email: "",
          password: ""
        }
      };
    }
  });
</script>

<style scoped>
  p {
    background-color: blue;
  }
</style>