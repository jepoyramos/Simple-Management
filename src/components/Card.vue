<template>
	<router-link :to="`/project/${cardID}`" class="c-card">
    <h2>{{cardTitle}}</h2></router-link>
</template>

<script>
export default {
  name: 'Card',
  props: {
    cardTitle: String,
    cardID: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
	.c-card{
		border: solid 1px #696969;
		border-radius: 5px;
		margin: 5px;
    text-decoration: none;
    color: #323659;
	}
</style>
