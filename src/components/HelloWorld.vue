<template>
  <div>
    <p>Child Component</p>
  </div>
</template>

<script>
export default {
  mounted() {
    setTimeout(() => {
      this.$emit('childEvent', 'Event emitted after 3 seconds');
    }, 3000);
  },
};
</script>
