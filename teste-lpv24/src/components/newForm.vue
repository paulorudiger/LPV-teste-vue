<template>
    {{ getMessage }} <br>
    {{ getMessageMet() }}<br>
    {{ mudou }}
    <button @click="change()"> MUDAR!!!? </button>
  </template>
  
  <script>
  export default {
    data: () => ({
      message: '',
      mudou: false
    }),
    computed: {
      getMessage() {
        return 'ola mundo computado' + this.message;
      }
    },
    methods: {
      getMessageMet() {
        return 'ola mundo methods!' + this.message;
      },
      change() {
        this.message = '     mudou!!!!!!!'
      }
    },
    watch: {
      message() {
        this.mudou = true;
      }
    }
  }
  </script>