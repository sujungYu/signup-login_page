<template>
  <div class="login">
    <h3>Login</h3>
    <input type="text" placeholder="아이디"><br>
    <input type="text" placeholder="비밀번호"><br>
    <button v-on:click="login">로그인</button>
    <p>만약에 계정이 없다면, <router-link to="/signup">회원가입</router-link>을 먼저 진행해주세요!</p>
  </div>
</template>

<script>
export default {
  name: 'login',
  data() {
    return{

    }
  },
  methods: {
    login() {
      this.$router.replace('home')
    }
  }

}
</script>

<style>
.login {
  margin-top: 40px;
}
input {
  margin: 10px 0;
  width: 20%;
  padding: 15px;
}
button {
  margin-top: 20px;
  width: 10%;
  cursor: pointer;
}
p {
  margin-top: 40px;
  font-size: 15px;
}
p a {
  text-decoration: underline;
  cursor: pointer;
}
</style>