<template>
  <div id="navbar">
      <nav class="header">
          <h1 class="heading">Welcome to Vue JS sample Project</h1>
          <h2>To - Do list application </h2>
      </nav>
    </div>
    <div class="footer bg-info">
     <h3 class="text-dark">Made using Vue Router & TypeScript ....</h3>
     <h4 class="text-dark">Styled using Bootstrap</h4>
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

.header {
  height: 30vh;
  background-color: #42b983;
  background-size: cover;
  border: 0;
  border-radius: 10px;
  color: #323f4b;
  font-family: roboto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.routes {
  margin: 15px;
}

.footer {
  background-color: blanchedalmond;
  color: #2c3e50;
  font-family: roboto;
  padding: 20px;
  border: 0;
  border-radius: 12px;
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
