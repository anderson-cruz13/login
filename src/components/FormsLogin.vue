<template>
  <div class="container">

    <template v-if="!name">
      <div class="description">
        Comece agora sua jornada no mundo 
        <span class="highlight">dev</span>, faça agora seu login e aproveite nosso curso 
        <span class="highlight">gratuito</span>!
      </div>
    </template>
    <template v-else>
      <div class="description">
        Muito bem
        <span class="highlight">{{name.toUpperCase()}}</span>, agora é só partir para sua viagem pelo aprendizado!
      </div>
    </template>

    <div class="login">
      <img class="logo" src="@/assets/rockt_icon.png">
  
      <div class="login-form">
        <input v-model="inputName" class="input" type="text" placeholder="Nome">
        <input v-model = "inputPassword" class="input" type="password" placeholder="Senha">
        <div class="button-text" @click="handleClick">Esqueceu sua senha?</div>
        <div v-if="inputName && inputPassword" class="button-login" @click="login">Partir</div>
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
      this.$emit('user-login', this.inputName);
      this.inputName = "";
      this.inputPassword = "";
    },
    signup() {
      console.log("Cadastra-se >")
    }
  }
}
</script>