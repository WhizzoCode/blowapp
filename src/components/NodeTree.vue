<template>
  <details v-for="item in treeitems" :key="item.id">
    <summary>{{ item.name }}</summary>
    <NodeTree :treeitems=item.children />
  </details>
</template>

<script>
export default {
  name: 'NodeTree',
  props: {
    treeitems: Object
  }
};
</script>

<style scoped>
</style>
