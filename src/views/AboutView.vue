<template>
  <div class="about">
    <get-commit-if/>
  </div>
</template>

<script>
// @ is an alias to /src
import GetCommitsIf from '@/components/GetCommitIf.vue'
export default {
  props: ['sha'],
  name: 'About',
  components: {
    GetCommitsIf
  }
}
</script>