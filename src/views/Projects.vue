<template>
  <div class="c-projects">
    <div class="o-projects__addProject">
    	<input type="text" v-model="newProject">
    	<button @click="addProject">Create Project</button>
    </div>
    <div class="o-projects__projectList" >
    	<Project v-for='(project, index) in projects' :key="index" :projectTitle="project.title"/>
    </div>
  </div>
</template>

<script>
import Project from '../components/Project.vue';
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
  	Project
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
  }
}
</script>
