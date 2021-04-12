<template>
  <div class="hello">
    <h1>{{ msg }}, {{ price }}</h1>
    <h2>{{ book.title }}/{{ book.author }}/{{ book.year }}</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";

interface Book {
  title: string;
  author: string;
  year: number;
}

// export interface User {
//   firstName: string;
//   lastName: string;
//   age: number;
// }

export default defineComponent({
  name: "HelloWorld",

  props: {
    msg: {
      type: String as PropType<string>,
      required: true,
    },
    price: {
      type: Number as PropType<number>,
      required: false,
    },
    // user: {
    //   type: Object as PropType<User>,
    // },
  },
  data() {
    return {
      book: {
        title: "Vue 3 Guide",
        author: "Vue Team",
        year: 2020,
      } as Book,
      //   firstName: "",
      //   lasttName: "",
      //   age: "",
      // } as User,
    };
  },
  // computed: {
  //   fullName(): string {
  //     return this.user.firstName + "" + this.user.firstName;
  //   },
  // },
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
  text-align: center;
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
