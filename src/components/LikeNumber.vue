<template>
<div>
 いいね（{{ halfNumber }}
<button @click="increment">+1</button>
</div>
</template>

<script>
export default {
//  props:["totalNumber"],
props: ['totalNumber','testNumber'],
 computed: {
   halfNumber() {
     return this.totalNumber / 2
   }
 },
  methods: {
    increment() {
      // this.number +=1;
      // 子から親へのデータの渡し口
      this.$emit("my-click", this.totalNumber + 1);
    }
  }
};
</script>
