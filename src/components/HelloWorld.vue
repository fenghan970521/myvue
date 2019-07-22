<template>
  <div class="hello">
    这是首页
    {{count}}
    <p>
      <button @click="increment">+增加</button>
      <button @click="decrement">-减少</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {};
  },
  created() {
    console.log(this.changePeople);
  },
  computed: {
    changePeople() {
      return this.$store.getters.changePeople;
    },
    count() {
      return this.$store.state.count;
    }
  },
  methods: {
    increment() {
      this.$store.commit("increment", 5);
    },
    decrement() {
      this.$store.commit("decrement", 5);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
