<template>
  <div class="hello">
    <div>Count is: {{ counter }}</div>
    <button type="button" @click="increment">Increment</button>
  </div>
</template>

<script>
import { mapMutations, mapState } from "vuex";

export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  computed: {
    ...mapState(["counter"]),
  },
  methods: {
    ...mapMutations(["increment"]),
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
