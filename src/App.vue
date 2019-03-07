<template>
  <div id="app">
    <h1 class="hb">{{Title}}</h1>
    <button class="key" v-on:click="changeArray">Pass a fixed array to the child component</button>
    <app-header v-bind:headerTitle="headerTitle"></app-header>
    <Users v-bind:users="users" v-show="key"></Users>
    <modify v-on:titleChange="changeTitle($event)" v-on:titleChangeTag="changeTitleTag($event)"></modify>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from "./components/header";
import Footer from "./components/footer";
import Users from "./components/user";
import modify from "./components/modify";
export default {
  name: "App",
  data() {
    return {
      key: false,
      headerTitle: "children-header",
      users: [
        { name: "jack", position: "父组件出来的值", show: false },
        { name: "rosen", position: "父组件出来的值", show: false },
        { name: "nike", position: "父组件出来的值", show: false },
        { name: "adidas", position: "父组件出来的值", show: false },
        { name: "marry", position: "父组件出来的值", show: false },
        { name: "herry", position: "父组件出来的值", show: false },
        { name: "kennig", position: "父组件出来的值", show: false },
        { name: "dancing", position: "父组件出来的值", show: false }
      ],
      Title: "Father Title"
    };
  },
  methods: {
    changeTitle(title) {
      this.Title = title;
    },
    changeArray() {
      this.key = true;
    },
    changeTitleTag(title) {
      this.headerTitle = title;
    }
  },
  components: {
    "app-header": Header,
    "app-footer": Footer,
    Users,
    modify
  }
};
</script>

<style>
#app {
  text-align: center;
}
h1 {
  color: red;
  text-align: center;
}
.key {
  padding: 10px;
  margin: 20px auto;
  border: 0;
  background: lightpink;
  border-radius: 4px;
}
</style>
