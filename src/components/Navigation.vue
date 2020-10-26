<template>
    <div class="sidenav">
        <h1>BackPack</h1>
        <a href="#Home"><i></i>Home</a>
        <a href="#services"><i></i>Library</a>
        <a href="#clients"><i></i>Create Study Set</a>
        <a href="#contact"><i></i>Settings</a>
        <a href="#contact" class="logout"><i></i>Logout</a>
    </div>
</template>
<script>
export default {
    name: 'Navigation',
}
</script>
<style scoped>
body {font-family: Arial, Helvetica, sans-serif;}
.sidenav {
  height: 100%;
  width: 15%;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  background-color: #fbf9fa;
  overflow-x: hidden;
  padding-top: 20px;
}

.sidenav h1{
  padding: 6px 8px 6px 16px;
  color: #bae9d3;
}

.sidenav a {
  padding: 6px 8px 6px 16px;
  text-decoration: none;
  font-size: 18px;
  color: #dad4dc;
  display: block;
}

.sidenav a:hover {
  color: #111;
}

.sidenav a.logout{
  margin-top: 200%;
}

.main {
  margin-left: 160px;
  font-size: 28px; 
  padding: 0px 10px;
}

</style>