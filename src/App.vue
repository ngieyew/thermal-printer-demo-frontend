<script>
import axios from "axios";

export default {
  data() {
    return {
      posts: [],
    };
  },
  mounted() {},
  methods: {
    print() {
      axios
        .post("http://127.0.0.1:3000/api/print", {})
        .then((response) => {
          console.log(response);
        })
        .catch((error) => {
          console.log("Error:", error);
        });
    },
  },
};
</script>

<template>
  <div>
    <h1>Print Receipt Demo</h1>

    <button @click="print">Print</button>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
