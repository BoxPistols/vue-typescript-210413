<template>
  <div class="hello">
    <h1>{{ msg }}, {{ price }}</h1>
    <h2>{{ book.title }}/{{ book.author }}/{{ book.year }}</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

interface Book {
  title: string;
  author: string;
  year: number;
}

export default defineComponent({
  name: "HelloWorld",
  props: {
    msg: String,
    price: Number,
  },
  data() {
    return {
      book: {
        title: "Vue 3 Guide",
        author: "Vue Team",
        year: 2020,
      } as Book,
    };
  },
  methods: {
    changeYear() {
      this.book.year = 1000;
    },
  },
  components: {},
});
</script>

<style scoped lang="scss">
.hello {
  h1 {
    margin: 40px 0 0;
    color: tomato;
  }
  h2 {
    color: teal;
  }
}
</style>


あああ
