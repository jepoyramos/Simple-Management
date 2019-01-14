<template>
  <div id="app" class="o-gridContainer o-grid--4col">
    <div class="c-sidebar">
      <div id="nav">
        <router-link to="/">Dashboard</router-link>
        <router-link to="/projects">Projects</router-link>
        <router-link to="/about">Tasks</router-link>
      </div>
    </div>
    <div class="c-mainView o-grid__column--3col">
      <router-view/>
    </div>
  </div>
</template>

<style lang="scss">
body{
  margin: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.o-gridContainer{
  display: grid;
}
.o-grid--4col{
  grid-template-columns: 1fr 1fr 1fr 1fr;
  -ms-grid-columns: 1fr 1fr 1fr 1fr;
}
.o-grid--3col{
  grid-template-columns: 1fr 1fr 1fr;
  -ms-grid-columns: 1fr 1fr 1fr;
}
.o-grid--2col{
  grid-template-columns: 1fr 1fr;
  -ms-grid-columns: 1fr 1fr;
}
.o-grid__column--4col{
  grid-column: auto / span 4;
  -ms-grid-column: auto / span 4;
}
.o-grid__column--3col{
  grid-column: auto / span 3;
  -ms-grid-column: auto / span 3;
}
.o-grid__column--2col{
  grid-column: auto / span 2;
  -ms-grid-column: auto / span 2;
}
.c-sidebar{
  background: #323659;
  height: 100vh;
}
.c-mainView{
  height: 100vh;
  overflow: scroll;
}
#nav {
  a {
    display: block;
    font-weight: bold;
    color: #ffffff;
    text-decoration: none;
    &.router-link-exact-active {
      background: #42b983;
    }
  }
}
</style>
