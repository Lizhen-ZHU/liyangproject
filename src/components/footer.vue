<template>
  <footer class="app-footer">
    <p>{{title}}</p>
  </footer>
</template>

<script>
export default {
  name: "",
  data() {
    return {
      title: "children footer"
    };
  }
};
</script>
<style scoped>
footer {
  background: #222;
  padding: 6px;
}
p {
  color: lightgreen;
  text-align: center;
}
</style>
