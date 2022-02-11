<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld
  }
};
</script>

<style>
:root {
  font-family: 'Source Sans 3 VF', sans-serif;

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

#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
