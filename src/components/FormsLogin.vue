<template>
  <div class="container">

    <div class ="description">
      <p>Welcome back</p>
    </div>

    <div class="login">
      <img class="logo" src="@/assets/rockt_icon.png">
  
      <div class="login-form">
        <input class="input" type="text" placeholder="Nome">
        <input class="input" type="password" placeholder="Password">
        <div class="button-text" @click="handleClick">Esqueceu sua senha?</div>
        <div class="button-login" @click="login">Partir</div>
        <div class="button-signup" @click="signup">Cadastra-se ></div>
      </div>
    </div>

  </div>
</template>

<script>
import '../styles.css'

export default {
  name: 'FormsLogin',
  props: ['name'],
  data () {
    return {
      inputName: "",
      inputPassword: "", 
    }
  },
  methods: {
    handleClick() {
      console.log("Esqueceu sua senha?")
    },
    login() {
      console.log("Partir")
    },
    signup() {
      console.log("Cadastra-se >")
    }
  }
}
</script>