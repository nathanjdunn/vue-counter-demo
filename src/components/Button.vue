<template>
  <div>
    <button @click="buttonClicked">{{ label }}</button>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String      
    },
    event: {
      type: String,
        validator: (val) => ['increment', 'decrement'].includes(val)
    }
  },
  methods: {
    buttonClicked() {
      this.$emit(this.event);
    }
  }
}
</script>

<style>
button {
  width: 3rem;
}
</style>
