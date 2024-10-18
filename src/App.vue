<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  data() {
    return {
      showChild: true,
      message: 'Waiting for event...',
    };
  },
  methods: {
    handleEvent(payload) {
      this.message = payload;
    },
    toggleChild() {
      this.showChild = !this.showChild;
    },
  },
components: {
    HelloWorld,
  },
};
</script>
<template>
    <div>
      <HelloWorld v-if="showChild" @childEvent="handleEvent" />
      <button @click="toggleChild">Toggle Child</button>
      <p>{{ message }}</p>
    </div>
  </template>
  
  