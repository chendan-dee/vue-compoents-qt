<template>
  <h3>Main</h3>
  <p>搜索内容为：{{ search }}</p>
  <searchComponent @searchEvent="getSearch" />
</template>
<script>
import searchComponent from "./searchComponent.vue";
export default {
  data() {
    return {
      search: "",
    };
  },
  components: {
    searchComponent,
  },
  methods: {
    getSearch(data) {
      this.search = data;
    },
  },
};
</script>
