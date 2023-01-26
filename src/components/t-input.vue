<template>
  <label class="block">
    <span class="font-medium text-gray-700">{{ label }}</span>
    <input
      class="mt-1 input-custom form-field ml-2 border border-gray-900"
      v-bind="$attrs"
      :type="type"
      :id="id"
      :name="name"
      v-on:input="$emit('input', $event.target.value)"
      :class="{'is-invalid': error, bg}"
    >
    <transition name="slide">
      <p v-show="error" class="invalid-feedback">{{ error }}</p>
    </transition>
  </label>
</template>

<script>
export default {
  name: "k-input",
  inheritAttrs: false,
  props: {
    error: {
      type: String,
      required: false
    },
    id: {
      type: String,
      required: false
    },
    name: {
      type: String,
      required: false
    },
    label: {
      type: String
    },
    bg: {
      type: String,
      required: false
    },
    type: {
      type: String,
      default: "text",
      validator: val => {
        return (
          ["url", "text", "password", "email", "search"].indexOf(val) !== -1
        );
      }
    }
  },
  methods: {
    updateValue(e) {
      this.$emit("input", e.target.value);
    }
  }
};
</script>