<template>
	<router-link to="/project/:cardID" class="c-card">
    <h2>{{cardTitle}}</h2>
    <h2>{{cardID}}</h2>
 	</router-link>
</template>

<script>
export default {
  name: 'Card',
  props: {
    cardTitle: String,
    cardID: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
	.c-card{
		border: solid 1px #696969;
		border-radius: 5px;
		margin: 5px;
	}
</style>
