<template>
  <Menubar />
  <div id="frames">
    <div id="left-pane" class="pane">
      <Tree :treeitems=treeItems />
    </div>
    <div id="content"></div>
    <div id="right-pane" class="pane"></div>
  </div>
</template>

<script>
import Menubar from './components/Menubar.vue';
import Tree from './components/Tree.vue';

export default {
  name: 'App',
  components: {
    Menubar,
    Tree
  },
  data() {
    return {
      treeItems: [
        {id: '0', name: 'Galería', children: [
          {id: '0-0', name: '2021', children: [
            {id: '0-0-0', name: '01', children: [
              {id: '0-0-0-0', name: '01'},
              {id: '0-0-0-1', name: '02'},
              {id: '0-0-0-2', name: '03'},
              {id: '0-0-0-3', name: '04'},
              {id: '0-0-0-4', name: '05'}
            ]},
            {id: '0-0-1', name: '02', children: [
              {id: '0-0-1-0', name: '01'},
              {id: '0-0-1-1', name: '02'},
              {id: '0-0-1-2', name: '03'},
              {id: '0-0-1-3', name: '04'},
              {id: '0-0-1-4', name: '05'}
            ]},
            {id: '0-0-2', name: '03', children: [
              {id: '0-0-2-0', name: '01'},
              {id: '0-0-2-1', name: '02'},
              {id: '0-0-2-2', name: '03'},
              {id: '0-0-2-3', name: '04'},
              {id: '0-0-2-4', name: '05'}
            ]}
          ]},
          {id: '0-1', name: '2022', children: [
            {id: '0-1-0', name: '01', children: [
              {id: '0-1-0-0', name: '01'},
              {id: '0-1-0-1', name: '02'},
              {id: '0-1-0-2', name: '03'},
              {id: '0-1-0-3', name: '04'},
              {id: '0-1-0-4', name: '05'}
            ]},
            {id: '0-1-1', name: '02', children: [
              {id: '0-1-1-0', name: '01'},
              {id: '0-1-1-1', name: '02'},
              {id: '0-1-1-2', name: '03'},
              {id: '0-1-1-3', name: '04'},
              {id: '0-1-1-4', name: '05'}
            ]},
            {id: '0-1-2', name: '03', children: [
              {id: '0-1-2-0', name: '01'},
              {id: '0-1-2-1', name: '02'},
              {id: '0-1-2-2', name: '03'},
              {id: '0-1-2-3', name: '04'},
              {id: '0-1-2-4', name: '05'}
            ]}
          ]}
        ]},
        {id: '1', name: 'Importaciones', children: [
          {id: '1-0', name: '2021-03-01'},
          {id: '1-1', name: '2021-03-02'},
          {id: '1-2', name: '2021-03-03'},
          {id: '1-3', name: '2021-03-04'},
        ]},
        {id: '2', name: 'Papelera'}
      ]
    };
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  line-height: 1;
}

:root {
  background-color: var(--gray-10);
  color: var(--gray-90);
  font-family: 'Source Sans 3 VF', sans-serif;
  font-size: 14px;

  --gray-0:   hsl(0, 0%,   0%);
  --gray-5:   hsl(0, 0%,   5%);
  --gray-10:  hsl(0, 0%,  10%);
  --gray-15:  hsl(0, 0%,  15%);
  --gray-20:  hsl(0, 0%,  20%);
  --gray-25:  hsl(0, 0%,  25%);
  --gray-30:  hsl(0, 0%,  30%);
  --gray-35:  hsl(0, 0%,  35%);
  --gray-40:  hsl(0, 0%,  40%);
  --gray-45:  hsl(0, 0%,  45%);
  --gray-50:  hsl(0, 0%,  50%);
  --gray-55:  hsl(0, 0%,  55%);
  --gray-60:  hsl(0, 0%,  60%);
  --gray-65:  hsl(0, 0%,  65%);
  --gray-70:  hsl(0, 0%,  70%);
  --gray-75:  hsl(0, 0%,  75%);
  --gray-80:  hsl(0, 0%,  80%);
  --gray-85:  hsl(0, 0%,  85%);
  --gray-90:  hsl(0, 0%,  90%);
  --gray-95:  hsl(0, 0%,  95%);
  --gray-100: hsl(0, 0%, 100%);
}

html, body, #app {
  height: 100%;
}

#app {
  display: flex;
  flex-direction: column;
}

#frames {
  flex-grow: 1;
  display: flex;
}

#content {
  flex-grow: 1;
}

.pane {
  width: 20rem;
  background-color: var(--gray-15);
}
</style>
