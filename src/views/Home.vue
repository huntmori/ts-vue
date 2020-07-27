<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <message></message>
    <children :parentMessage="message"></children>
  </div>
</template>

<script lang="ts">
  // @ is an alias to /src
  import {Component,Vue}  from 'vue-property-decorator';
  import message          from '@/components/Message.vue';
  import Children         from '@/components/Children.vue';
  @Component({
    components: {
      message, Children
    },
  })

  export default class Home extends Vue {
    message: string = 'hello home class';
  }
</script>
