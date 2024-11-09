<template>
  <div class="container">
    <FormsLogin v-bind:name="name" @user-login="updateName"/>
  </div>
</template>

<script>
import FormsLogin from './components/FormsLogin.vue'
import "@/styles.css"

export default {
  name: 'App',
  components: {
    FormsLogin
  },
  data (){
    return {
      name: "",
    }
  },
  methods: {
    updateName(name) {
      this.name = name;
    }
  }

}
</script>

