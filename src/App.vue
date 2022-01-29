<template>
    <div>
      <like-header></like-header>
      <h2>{{ number }}</h2>
      <like-number :total-number="number" v-on:my-click="incrementNumber"></like-number>
      <!-- 左側が子コンポーネントファイルで設定したpropsの受け口、右側が親コンポーネントで設定したdata。 -->
      <like-number :total-number="number" :test-number="testNumber"></like-number>
    </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import LikeNumber from './components/LikeNumber.vue'
import LikeHeader from './components/LikeHeader.vue'

export default {
  data() {
    return {
        number:14,
        // testNumber:24
    };
  },
  components: {
    LikeNumber,
    LikeHeader
  },
  methods:{
    incrementNumber(value) {
      this.number = value
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
