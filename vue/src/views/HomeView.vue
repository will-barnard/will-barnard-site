<template>
  <div class="top">
    <header>
      <h1>Will Barnard</h1>
      <img src="/img/headshot.png"/>
    </header>

  <div class="subheader">
    <h2>Software&nbsp;Developer</h2>
    <div class="container" id="contact">
      <div class="subcontainer">
        <a href="https://www.linkedin.com/in/will-barnard-dev/" target="_blank">🔗&nbsp;LinkedIn</a>
      </div>
      <div class="subcontainer">
        <a href="/will-barnard-resume.pdf" target="_blank">🔗&nbsp;Resume</a>
      </div>
      <div class="subcontainer">
        <a href="https://github.com/will-barnard" target="_blank">🔗&nbsp;GitHub</a>
      </div>
    </div>
    
    <AboutMe />
    
  </div>
  

  </div>
  <main>
    <div class="major-projects-section">
      <h1>Major Projects</h1>
      <div class="tile-container">
        <ProjectTile v-for="project in majorProjects" :key="project.id" :project="project" class="tile"/>
      </div>
    </div>
    <div class="minor-projects-section">
      <h1>Minor Projects</h1>
      <div class="tile-container">
        <ProjectTile v-for="project in minorProjects" :key="project.id" :project="project" class="tile"/>
      </div>
    </div>
  </main>

</template>

<script>
import AboutMe from '../components/AboutMe.vue';
import ProjectTile from '../components/ProjectTile.vue';
import Projects from '../assets/Projects.js';

export default {
  components: {AboutMe, ProjectTile},
  data() {
    return{
      majorProjects: [],
      minorProjects: []
    }
  },
  created() {
    this.majorProjects = Projects.majorProjects;
    this.minorProjects = Projects.minorProjects;
  },
  methods: {
  
  }
}

</script>

<style scoped>
.top {
  background-color: var(--vt-c-black-mute);
  display: flex;
  flex-direction: column;
  border-radius: 15px;
  padding: 20px;
  margin-bottom: 20px;
}
header {
  text-align: center;
  font-size: 5vw;
  margin-bottom: 20px;
}
header img {
  width: 65vw;
  border-radius: 15px;
}
h2 {
  font-size: 6vw;
  margin-bottom: 20px;
}
h3 {
  text-align: center;
  font-size: 6vw;
}
.subheader {
  font-size: 1.2em;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-bottom: 20px;
}
.container {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: nowrap;
  border-radius: 10px;
  margin-bottom: 20px;
}
#contact {
  width: 100%;
  margin: 20px 0;
  font-size: 1em;
}
.subcontainer p{
  margin: 15px;
  text-align: left;
  width: 100%;
}
.subcontainer:hover {
  cursor: pointer;
}
.tile {
  border: 2px solid;
  border-radius: 15px;
  padding: 20px;
  margin: 15px;
  transition: transform 0.3s;
}
.tile:hover {
  transform: scale(1.05);
}
.tile-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: start;
  flex-wrap: wrap;
}
.major-projects-section {
  background-color: #383838;
  padding: 20px;
  border-radius: 15px;
  margin-bottom: 20px;
}
.minor-projects-section {
  padding: 20px;
  border-radius: 15px;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    flex-direction: row-reverse;
    justify-content: center;
    align-items: center;
  }
  header h1 {
    margin: 30px;
    font-size: 6vw;
  }
  header img {
    width: 30vw;
  }
  h3 {
    font-size: 5vw;
  }
  .subheader h2 {
    font-size: 4vw;
  }
  .subheader a {
    font-size: 2em;
  }
  #contact {
    width: 50vw;
  }
  .tile {
    width: 30vw;
  }
}

</style>