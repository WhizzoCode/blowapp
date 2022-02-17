<template>
  <div class="nodetree">
    <div class="summary" @click="toggle" :style="{paddingLeft: `${ indentation }rem`}">
      <div class="expander" :style="{visibility: haschildren ? 'visible' : 'hidden'}">
        <i class="ri-arrow-right-s-line"></i>
      </div>
      <div class="label">{{ treeitems.name }}</div>
    </div>
    <div class="content" v-show="open">
      <NodeTree
        v-for="child in treeitems.children"
        :key="child.id"
        :treeitems="child"
        :indentation="indentation + 1"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'NodeTree',
  props: {
    treeitems: Object,
    indentation: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {
      open: false
    };
  },
  computed: {
    haschildren() {
      return this.treeitems.children?.length > 0;
    }
  },
  methods: {
    toggle() {
      if (this.haschildren) this.open = !this.open;
    }
  }
};
</script>

<style scoped>
.summary {
  display: flex;
  cursor: pointer;
}

.summary:hover {
  background-color: var(--gray-25);
}

.expander:not(.children) {
  visibility: hidden;
}
</style>
