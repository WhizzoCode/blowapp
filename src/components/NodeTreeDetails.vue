<template>
  <div :style="cssVars">
    <details v-if="hasChildren" :open="isDetailsOpen">
      <summary>{{ treeitems.name }}</summary>
      <div v-for="child in treeitems.children" :key="child.path">
        <NodeTreeDetails
          :treeitems="child"
          :indentation="this.indentation + 1"
        />
      </div>
    </details>
    <p v-else>{{ treeitems.name }}</p>
  </div>
</template>

<script>
export default {
  name: 'NodeTreeDetails',
  props: {
    treeitems: Object,
    indentation: {
      type: Number,
      default: 0
    },
    parentOpen: {
      type: Boolean,
      default: true
    }
  },
  data() {
    return {
      isDetailsOpen: false
    };
  },
  computed: {
    hasChildren() {
      return this.treeitems.children?.length > 0;
    },
    cssVars() {
      return {
        '--indentation': `${ this.indentation }rem`
      };
    }
  }
};
</script>

<style scoped>
summary {
  position: relative;
  list-style-type: none;
}

summary::before {
  position: absolute;
  left: var(--indentation);
  font-family: 'remixicon';
  content: '\ea6e';
}

details[open] > summary::before{
  transform: rotate(90deg);
}

summary,
p {
  padding-left: calc(var(--indentation) + 1rem);
  cursor: pointer;
}

summary:hover,
p:hover {
  background-color: var(--gray-25);
}
</style>
