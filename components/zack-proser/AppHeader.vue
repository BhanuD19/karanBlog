<template>
    <header class="header-global">
      
<!--Navigation-->
<nav class="nav" v-bind:class= "{collapsee : isToggled}">
  <div class="nav-menu flex-rowe">
    <div class="nav-brand">
      <nuxt-link to="/" class="text-gray">
      <img src="/logo.png">
      </nuxt-link>
      <span><nuxt-link to="/" class="text-gray"> Karan's Blog </nuxt-link></span>
    </div>
<!--    Todo: add toggle-menu icon-->
    <div class="toggle-collapse">
      <div class="toggle-icon">
        <i class="fas fa-bars" @click="isToggled = !isToggled"></i>
      </div>
    </div>
    <div>
      <ul class="nav-items">
        <li class="nav-link">
          <nuxt-link to="/about">About</nuxt-link>
        </li>
        <li class="nav-link">
          <nuxt-link to="/software">Blogs</nuxt-link>
        </li>
        <li class="nav-link">
          <nuxt-link to="/services">Services</nuxt-link>
        </li>
        <li class="nav-link">
          <nuxt-link to="/contact">Contact Us</nuxt-link>
        </li>
      </ul>
    </div>
    <div class="social text-gray">
      <i class="fab fa-facebook-square"></i>
      <i class="fab fa-instagram-square"></i>
      <i class="fab fa-twitter-square"></i>
      <i class="fab fa-youtube-square"></i>
    </div>
  </div>
</nav>
<!--X-Navigation-X-->
    </header>
</template>
<script>


export default {
  data() {
    return {
      isToggled: false
    }
  }
};
</script>
<style scoped>
/*Navbar*/

.nav {
  background: white;
  padding: 0 2rem;
  width: 100%;
  height: 0rem;
  min-height: 10vh;
  overflow: hidden;

  /*To add to toggle menu*/
  transition: height 1s ease-in-out;
}

.nav .nav-menu {
  width: 100%;
  justify-content: space-between;
}

.nav .toggle-collapse {
  position: absolute;
  top: 0%;
  width: 90%;
  cursor: pointer;
  display: none;
}

.nav .toggle-collapse .toggle-icon {
  display: flex;
  justify-content: flex-end;
  padding: 1.7rem 0;

  font-size: 1.4rem;
  color: var(--text-gray);
}

.collapsee {
  height: 30rem;
}

.nav .nav-items {
  display: flex;
  margin: 0;
}

.nav .nav-items .nav-link {
  padding: 1.6rem 1rem;
  font-size: 1.1rem;
  position: relative;
  font-family: var(--Abel);
}
/*Hover effects for nav-links*/
.nav .nav-items .nav-link:hover {
  background-color: var(--midnight) !important;
}

.nav .nav-items .nav-link:hover a {
  color: white !important;
}

.nav .nav-brand {
  display: flex;
  margin: 0;
}

.nav .nav-brand span {
  padding: 0.5rem 0.7rem;
  font-size: 1.1rem;
  position: relative;
  font-family: var(--Abel);
}

.nav .nav-brand a{
  font-size: 1.6rem;
  padding: 1rem 0;
  text-decoration: none;
  display: block;
  font-family: var(--Lex);
}

.nav .nav-brand span a :hover {
  color: var(--text-gray) !important; 
}

.nav .nav-brand a img {
  height: 40px;
  width: 80px;
}

.nav .social {
  padding: 1.4rem 0.2rem;
}
.nav .social i {
  padding: 0 0.2rem;
}
/*Hover effect for social links*/
.nav .social i:hover {
  cursor: pointer;
  color: #a1c4cf;
}

/*X-Navbar-X*/

/*Viewport less than or equal to 750px*/

@media only screen and (max-width: 750px) {

  .nav .nav-menu, .nav .nav-items {
    flex-direction: column;
  }

  .nav .toggle-collapse {
    display: initial;
  }
}

/*Viewport less than or equal to 520px*/

@media only screen and (max-width: 520px){
  .nav .toggle-collapse {
    width: 80% !important;
  }

  .nav .nav-brand span {
    display: none;
  }
}


</style>
