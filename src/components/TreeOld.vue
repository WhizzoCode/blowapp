<template>
  <details v-for="item in treeitems" :key="item.id">
    <summary><div>{{ item.name }}</div></summary>
    <Tree :treeitems=item.children />
  </details>
  <!-- <i class="ri-arrow-right-s-line"></i> -->
</template>

<script>
export default {
  name: 'Tree',
  props: {
    treeitems: Object
  }
};
</script>

<style scoped>
details {
  position: relative;
}

details details {
  padding-left: 1rem;
}

summary {
  list-style-type: none;
  cursor: pointer;
  
  padding-left: 1rem;
}

summary:hover {
  background-color: var(--gray-25);
}

summary::before {
  font-family: 'remixicon';
  content: "\ea6e";
  position: absolute;
  left: 0rem;
}

details[open] > summary::before {
  transform: rotate(90deg);
}
</style>
