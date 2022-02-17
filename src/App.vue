<template>
  <Menubar />
  <div id="frames">
    <div id="left-pane" class="pane">
      <NodeTree :treeitems="galleryTree" />
      <NodeTree :treeitems="importsTree" />
      <NodeTree :treeitems="recycleBinTree" />
    </div>
    <div id="content"></div>
    <div id="right-pane" class="pane"></div>
  </div>
</template>

<script>
import Menubar from './components/Menubar.vue';
import NodeTree from './components/NodeTree.vue';

export default {
  name: 'App',
  components: {
    Menubar,
    NodeTree
  },
  data() {
    return {
      galleryTree: {
        id: 'Galería', name: 'Galería', children: [
          {id: 'Galería/2021', name: '2021', children: [
            {id: 'Galería/2021/01', name: '01', children: [
              {id: 'Galería/2021/01/01', name: '01'},
              {id: 'Galería/2021/01/02', name: '02'},
              {id: 'Galería/2021/01/03', name: '03'},
              {id: 'Galería/2021/01/04', name: '04'},
              {id: 'Galería/2021/01/05', name: '05'}
            ]},
            {id: 'Galería/2021/02', name: '02', children: [
              {id: 'Galería/2021/02/01', name: '01'},
              {id: 'Galería/2021/02/02', name: '02'},
              {id: 'Galería/2021/02/03', name: '03'},
              {id: 'Galería/2021/02/04', name: '04'},
              {id: 'Galería/2021/02/05', name: '05'}
            ]},
            {id: 'Galería/2021/03', name: '03', children: [
              {id: 'Galería/2021/03/01', name: '01'},
              {id: 'Galería/2021/03/02', name: '02'},
              {id: 'Galería/2021/03/03', name: '03'},
              {id: 'Galería/2021/03/04', name: '04'},
              {id: 'Galería/2021/03/05', name: '05'}
            ]}
          ]},
          {id: 'Galería/2022', name: '2022', children: [
            {id: 'Galería/2022/01', name: '01', children: [
              {id: 'Galería/2022/01/01', name: '01'},
              {id: 'Galería/2022/01/02', name: '02'},
              {id: 'Galería/2022/01/03', name: '03'},
              {id: 'Galería/2022/01/04', name: '04'},
              {id: 'Galería/2022/01/05', name: '05'}
            ]},
            {id: 'Galería/2022/02', name: '02', children: [
              {id: 'Galería/2022/02/01', name: '01'},
              {id: 'Galería/2022/02/02', name: '02'},
              {id: 'Galería/2022/02/03', name: '03'},
              {id: 'Galería/2022/02/04', name: '04'},
              {id: 'Galería/2022/02/05', name: '05'}
            ]},
            {id: 'Galería/2022/03', name: '03', children: [
              {id: 'Galería/2022/03/01', name: '01'},
              {id: 'Galería/2022/03/02', name: '02'},
              {id: 'Galería/2022/03/03', name: '03'},
              {id: 'Galería/2022/03/04', name: '04'},
              {id: 'Galería/2022/03/05', name: '05'}
            ]}
          ]}
        ]
      },
      importsTree: {
        id: 'Importaciones', name: 'Importaciones', children: [
          {id: 'Importaciones/2021-03-01', name: '2021-03-01'},
          {id: 'Importaciones/2021-03-02', name: '2021-03-02'},
          {id: 'Importaciones/2021-03-03', name: '2021-03-03'},
          {id: 'Importaciones/2021-03-04', name: '2021-03-04'},
        ]
      },
      recycleBinTree: {id: 'Papelera', name: 'Papelera'}
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
