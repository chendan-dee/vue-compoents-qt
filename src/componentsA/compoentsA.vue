<template>
  <h3>compoentsA</h3>
  <compoentsB :title="title" :age="age" :names="names" />
</template>
<script>
import compoentsB from "./compoentsB.vue";
export default {
  data() {
    return {
      title: "这个是标题",
      age: 20,
      names: ["iwen", "ime"],
    };
  },
  //在组件的components选项中定义局部组件，该组件只能在定义它的父组件模板中使用。
  components: {
    compoentsB,
  },
};
</script>
