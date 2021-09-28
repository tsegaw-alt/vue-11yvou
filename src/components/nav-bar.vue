<template>
  <link rel="stylesheet" href="//cdn.jsdelivr.net/fontawesome/4.2.0/css/font-awesome.min.css" />
<link href='https://fonts.googleapis.com/css?family=Slabo+27px|Open+Sans' rel='stylesheet' type='text/css'>
<nav>
  <ul id="header">
    <a href="#" id="brand">
      <li>
       LOGOIPSUM
      </li>
    </a>
    <label id="trigger2" for="x7"><i class="fa fa-bars"></i></label>
  </ul>
  <input type="checkbox" id="x7"  v-show:"false"/>
  <ul id="main">
  
     <router-link to="/"><li>Dashboard</li></router-link>
    
   
    
              <router-link to="/events"><li>Events</li></router-link>

              <router-link to="/help"><li>Help</li></router-link>
              <router-link to="/logout"><li>Logout</li></router-link>
   
    </ul>
  </ul>
</nav>
<main>
 
</main>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped>

#header {
  left: 0;
  float: left;
  width: auto;
  z-index: 1000;
}
#caret {
  display: inline-block;
  height: 7px;
  width: 7px;
  border-left: 3px solid #fff;
  border-bottom: 3px solid #fff;
  transform: rotate(-45deg) translateY(-4px);
}

li, #trigger2, #trigger {
  top:0;
  list-style-type: none;
  display: inline-block;
  padding: 13px;
  color: #f2f2f2;
  transition: 0.2s;
}
ul {
  margin-top: 0;
  position: absolute;
  top: 0;
  background: #5C524D;
  display: block;
  width: 100%;
  height: 3em;
  text-align: right;
  padding-left: 0;
  padding-right: 0;
  
}
#main {
  left: 0;
  
}

a {
  text-decoration: none;
}
#dwn {
  font-size: 0.8em;
}
#trigger:hover + #dropdown, #dropdown:hover {
  height: 12em;
}
main {
  position: absolute;
  top: 2.8em;
}


.x1 {
  position: relative;
  top: -0.8em;
}
#src {
  text-decoration: underline;
}

#trigger2 {
  display: none !important;
}
#x7 {
  left: 999999px;
  
}
@media (max-width: 627px) {
  #header {
    width: 100%;
  }
  #brand {
    position: absolute;
    top: 0;
    left: 0;
  }
  #main {
    height: 0;
    overflow: hidden;
    z-index: 3000;
    top: 3em;
    text-align: left;
    transition: 0.5s;
  }
  #main li, #trigger {
    display: block;
  }
  
  #trigger2 {
    display: inline-block !important;
    position: absolute;
    top: 0;
    right: 0;
    cursor: pointer;

  }
  #x7:checked + #main {
    height:100%;

    padding-top: 1em;
  }
  
}



</style>