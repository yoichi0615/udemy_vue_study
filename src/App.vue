<template>
  <div class="main">
    <button @click="show = !show">
        切り替え
    </button>
    <transition name="fade">
    <p v-if="show">hello</p>
    </transition>

  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  data() {
    return {
        show:true,
    };
  },
  methods:{
    incrementNumber(value) {
      this.number = value
    }
  }
}
</script>

<style scoped>
.main {
  text-align: center;
  padding-top: 5rem;
  width: 70%;
  margin:auto;
}

.fade-enter{
  opacity: 0;
}
.fade-enter-active{
  transition: opacity 2s;
}
.fade-enter-to{
  opacity: 1;
}
.fade-leave{
  opacity: 1;
}
.fade-leave-active{
  transition: opacity 2s;
}
.fade-leave-to{
  opacity: 0;
}

</style>
