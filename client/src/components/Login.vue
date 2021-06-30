<template>
  <div class="login-background">
    <h3>Login</h3>
    <input  label="username" placeholder="username" v-model="rawUsername"  />
    <input type="password" label="password" v-model="rawPassword" placeholder="password" />
    <button v-on:click="login">Login</button>
    <div>
    </div>
  </div>
</template>


<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {},
})
export default class Login extends Vue {

  username = "";
  password = "";
  login(): void {
    console.log(this.username);
    console.log(this.password);
  }

  get rawUsername() {
    return this.rawUsername;
  }

  set rawUsername(value: string) {
    this.password = value;
  }

  get rawPassword() {
    return this.rawPassword;
  }

  set rawPassword(value: string) {
    this.username = value;
  }
}
</script>


<style lang="scss">
  .login-background {
    background: grey;
    display: flex;
    flex-direction: column;
  }

  input {
    height: 40px;
    margin: 10px 20px;
  }

  button {
    height: 40px;
  }
</style>