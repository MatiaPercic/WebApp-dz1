<template>
  <div class="home">
    
    <HelloWorld msg="Welcome to a displpay of commits"/>
    <get-commit/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import GetCommit from '@/components/GetCommit.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    GetCommit
  }
}
</script>
