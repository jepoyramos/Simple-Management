<template>
  <div class="c-project">
    <Project :projectTitle=""/>
  </div>
</template>

<script>
import Project from '../components/Project.vue';

export default {
  name: 'Project',
  data () {
  	return {
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
    projectID(){
      return index+1;
    }
  }
}
</script>
