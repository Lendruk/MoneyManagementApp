<template>
  <div class="home-container">
    <Login />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Login from "@/components/Login.vue"; // @ is an alias to /src

@Options({
  components: {
    Login,
  },
})
export default class Home extends Vue {}
</script>

<style lang="scss">
  .home-container {
    display: flex;
    width: 100%;
    justify-content: center;
    height: 100%;
    align-items: center;
    background: red;
  }
</style>
