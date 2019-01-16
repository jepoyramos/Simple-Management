<template>
  <div class="c-project">
    <h1>{{projectTitle}}</h1>
    <p>{{projectDescription}}</p>
    <h2>Project ID:{{ this.$route.params.id }}</h2>
    
  </div>
</template>

<script>

export default {
  name: 'Project',
  props: {
    projectTitle: String,
  },
  components: {},
  methods: {},
  computed: {}
}
</script>
