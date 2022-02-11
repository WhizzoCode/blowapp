<template>
  <ul>
    <li v-for="item in menubarItems" :key="item.id">
      {{ item.name }}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Menubar',
  data() {
    return {
      menubarItems: [
        {id: 0, name: 'Archivo'},
        {id: 1, name: 'Editar'},
        {id: 2, name: 'Ver'},
        {id: 3, name: 'Fotos'},
        {id: 4, name: 'Eventos'},
        {id: 5, name: 'Etiquetas'},
        {id: 6, name: 'Ayuda'}
      ]
    };
  }
};
</script>

<style scoped>
ul {
  background-color: var(--gray-20);
  display: flex;
  list-style: none;
}

li {
  padding: 0.5rem 1rem;
}

li:hover {
  background-color: var(--gray-30);
  cursor: pointer;
}
</style>
