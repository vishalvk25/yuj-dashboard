<template>
    <nav class="navbar navbar-expand-sm bg-dark navbar-dark">
  <ul class="navbar-nav">
    <li class="nav-item active">
      <a class="nav-link"><i class="fa fa-tachometer" aria-hidden="true"></i> DASHBOARD</a>
    </li>
   
  </ul>
 
</nav>

</template>

<script>
export default {
  name: 'Navbar',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
i.fa.fa-tachometer {
    color: #e77e3a;
}
.bg-dark{
  background-color: #000000 !important;
}
</style>
