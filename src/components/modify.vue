<template>
  <div class="modify">
    <input type="text" placeholder="Chang Father Title" v-model="content">
    <button v-on:click="changeTitle">Sure to change Tile</button>
    <br>
    <br>
    <input type="text" placeholder="Change Children Title" v-model="contentTag">
    <button v-on:click="changeTitleTag">Sure to change Tile</button>
  </div>
</template>

<script>
export default {
  name: "",
  data() {
    return {
      content: ""
    };
  },
  methods: {
    changeTitle() {
      this.$emit("titleChange", this.content);
    },
    changeTitleTag() {
      this.$emit("titleChangeTag", this.contentTag);
    }
  }
};
</script>
<style scoped>
.modify {
  max-width: 1200px;
  width: 100%;
  margin: 20px auto;
  padding: 20px;
  text-align: center;
}
input {
  width: 300px;
  height: 30px;
}
button {
  width: 80px;
  height: 32px;
  background: lightgreen;
  border: 0;
  border-radius: 4px;
}
</style>
