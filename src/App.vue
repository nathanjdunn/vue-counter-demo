<template>
  <div id="app">
    <Button label="+" event="increment" @increment="incrementCount" />
    <Button label="-" event="decrement" @decrement="decrementCount" />

    {{ count }}
  </div>
</template>

<script>
import Button from './components/Button.vue'

export default {
  name: 'app',
  data: function () {
    return {
      count: 0,
    }
  },
  components: {
    Button
  },
  methods: {
    incrementCount() {
      this.count++;
    },
    decrementCount() {
      this.count--;
    }    
  }
}
</script>

<style>
* {
  font-size: 1.5rem;
}
</style>
