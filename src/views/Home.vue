<template>
  <div class="home">
    <h1>This is an home page</h1>
    <input v-model="name" />
    <a href="javascript:" @click="addToList">ADD</a>
  </div>
</template>

<script>
import globalSrv from "../services/common.srv.js";

export default {
  name: "home",
  data: function() {
    return {
      name: ""
    };
  },
  methods: {
    addToList() {
      if (this.name != "") {
        globalSrv.myList.push(this.name);
      }
      this.name = "";
    }
  }
};
</script>
