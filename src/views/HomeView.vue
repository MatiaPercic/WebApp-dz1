<template>
  <div class="home">
    
    <HelloWorld msg="Welcome to a page for displayinig git commits"/>
    <get-commit/>
  </div>
</template>

<script>
// @ is an alias to /src
import GetCommit from '@/components/GetCommit.vue'

export default {
  name: 'HomeView',
  components: {
   
    GetCommit
  }
}
</script>
