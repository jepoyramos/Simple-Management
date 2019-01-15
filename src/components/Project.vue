<template>
  <div class="c-project">
    <h2>{{projectTitle}} " Project view"</h2>
    <p>{{projectDescription}}</p>
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
