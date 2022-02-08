<template>
  <div id="navbar">
      <div class="routing-container">
        <router-link to="/" class="routes">Home</router-link>
        <router-link to="/app" class="routes">To-do App</router-link>
      </div>
      <router-view/>
    </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.routes {
  margin: 15px;
}

#navbar {
  padding: 30px;
}

.routing-container {
  height: 10vh;
  padding: 20px;
  margin: 12px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 12px;
  border: 2px #323f4b solid;
}

#navbar a {
  font-weight: bold;
  color: #2c3e50;
}

#navbar a.router-link-exact-active {
  color: #42b983;
}
</style>
