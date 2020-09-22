<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style>
*  {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  font-family: 'Inter', 'Arial', sans-serif;
  font-style: normal;
  background-color: #FAF3F3;
}

img {
  max-width: 100%;
  height: auto;
}

#app {
  /*border: 7px solid #fff;
  border-radius: 40px;*/
  margin: 0 auto;
  max-width: 350px;
}

h1 {
  font-weight: 800;
  font-size: 22px;
  line-height: 30px;
  letter-spacing: 0.02em;
  text-align: center;
  color: #181C43;
  margin-top: 60px;
  margin-bottom: 20px;
}
</style>
