<template>
  <div class="c-projects">
    <div class="o-projects__addProject">
    	<input type="text" v-model="newProject">
    	<button @click="addProject">Create Project</button>
    </div>
    <div class="o-projects__projectList o-gridContainer o-grid--3col" >
    	<Card v-for='(project, index) in projects' :key="index" :cardTitle="project.title" :cardID="cardID(index)"/>
    </div>
  </div>
</template>

<script>
import Card from '../components/Card.vue';

export default {
  name: 'Projects',
  data () {
  	return {
  		newProject: '',
  		projects: [
				{title: 'Project 1'},
				{title: 'Project 2'},
  		],
  	}
  },
  components: {
    Card
  },
  methods: {
		addProject(){
			if (this.newProject != '') {
				this.projects.push({"title": this.newProject});
				this.newProject='';
			}else{
				alert('Please add project title');
			}
		}
  },
  computed: {
    cardID(index){
      return index+1;
    }
  }
}
</script>
