<template>
  <div class="c-project">
    <h2>{{projectTitle}} " Project Title"</h2>
    <p>{{projectDescription}}</p>
     <h2>Project ID:{{ this.$route.params.id }}</h2>
    
  </div>
</template>

<script>
export default {
  name: 'Project',
  props: {
    projectTitle: String,
    projectDescription: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
