<template>
  <div class="about">
    <h1>This is an about page</h1>
    <li :key="item" v-for="item in list">{{ item }}</li>
  </div>
</template>

<script>
import globalSrv from "../services/common.srv.js";

export default {
  name: "about",
  data: function() {
    return {
      list: globalSrv.myList
    };
  }
};
</script>