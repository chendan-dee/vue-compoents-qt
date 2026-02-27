<template>
  <h3>compoentsB</h3>
  <p>{{ title }}</p>
  <p>{{ age }}</p>
  <p v-for="(name, index) of names">{{ name }}</p>
  <button @click="updateHandle">修改数据</button>
</template>
<script>
export default {
  data() {
    return {};
  },
  props: {
    title: {
      type: [String, Number, Array, Object],
      // 标识必选项
      // required: true,
      default: "emmm",
    },
    age: {
      type: Number,
      default: 0,
    },
    //数字和字符串可以直接default，但是如果是数组和对象，必须通过工厂函数返回默认值
    names: {
      type: Array,
      default() {
        return ["空"];
      },
    },
  },
  methods: {
    updateHandle() {
      //错误操作,不允许修改父元素传递过来的数据
      console.log(this.title);
      this.title = "新数据";
    },
  },
};
</script>
