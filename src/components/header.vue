<template>
  <header class="app-header">
    <p>{{headerTitle}}</p>
  </header>
</template>

<script>
export default {
  name: "",
  props: ["headerTitle"],
  data() {
    return {
      title: "我是子组件1header"
    };
  }
};
</script>
<style scoped>
header {
  background: lightgreen;
  padding: 6px;
}
p {
  color: #222;
  text-align: center;
}
</style>
