<template>
  <h3>Parent</h3>
  <Child :title="message" :age="age" :names="names" :userInfo="userInfo" />
</template>

<script>
import Child from "./child.vue";
export default {
  data() {
    return {
      message: "Parents数据!",
      age: 10,
      names: ["any", "suger", "tomato"],
      userInfo: {
        name: "tome",
        age: 66,
      },
    };
  },
  components: {
    Child,
  },
};
</script>
