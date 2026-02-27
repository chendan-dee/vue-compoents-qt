<template>
  <h3>ChildEvent</h3>
  <button @click="clickEventHandle">传递数据</button>
</template>
<script>
export default {
  data() {
    return {
      msg: "child数据!",
    };
  },
  methods: {
    clickEventHandle() {
      //自定义事件
      this.$emit("someEvent", this.msg);
    },
  },
};
</script>
