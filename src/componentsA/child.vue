<template>
  <h3>Child</h3>
  <p>{{ title }}</p>
  <p>{{ age }}</p>
  <ul>
    <li v-for="(item, index) of names" :key="index">{{ item }}</li>
  </ul>
  <p>{{ userInfo.name }}</p>
  <p>{{ userInfo.age }}</p>
</template>

<script>
export default {
  props: ["title", "age", "names", "userInfo"],
};
</script>
