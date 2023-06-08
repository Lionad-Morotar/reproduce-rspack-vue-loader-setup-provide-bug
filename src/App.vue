<script lang="ts">
import HelloWorld from "./components/HelloWorld.vue";

let title: string = "Rspack + Vue";

export default {
  components: { HelloWorld },
  setup() {
    console.log(name);
    return {
      title,
      name,
    };
  },
};
</script>

<template>
  <div>
    <span>my-vars:</span>
    <span>{{ name.get() }}</span>
  </div>
  <HelloWorld :msg="title + name.get()" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
