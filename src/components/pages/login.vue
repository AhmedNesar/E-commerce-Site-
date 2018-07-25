<template>
  <div class="login">
    <div class="loginHeader" align="center">LOGIN</div>
    <div class="loginContainer">
      <table>
        <tr>
          <td>Username</td>
          <td>:</td>
          <td><input type="text" placeholder="username...." v-model="user.username"></td>
        </tr>
        <tr>
          <td>Password</td>
          <td>:</td>
          <td><input type="password" placeholder="password...." v-model="user.username"></td>
        </tr>
        <tr>
          <td colspan="3" align="center"><button class="addBtn" @click="loginNow()">Log Me In</button></td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: 'login',
  data () {
    return {
      user: {
        username: "",
        password:""
      }
    }
  },
  methods: {
    loginNow(){
      // console.log(this.user)
      this.$eventBus.$emit("loadingStatus", true);
    }
  }
}
</script>


