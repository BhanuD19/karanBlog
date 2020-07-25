<template>

<footer class="footere">
  <div class="containere">
    <div class="about-us" data-aos="fade-right" data-aos-delay="200">
      <h2>About Us</h2>
      <button class="btn btn-blog"><a href=#>Explore Posts</a></button>
    </div>
    <div class="newsletter" data-aos="fade-right" data-aos-delay="200">
      <h2>Newsletter</h2>
      <p>Stay updated with our latest!</p>
      <div class="form-element">
        <input type="text" placeholder="Enter your email!">
        <span><i class="fas fa-chevron-right"></i></span>
      </div>
    </div>
    <div class="instagram" data-aos="fade-left" data-aos-delay="200"> 
      <h2>Instagram</h2>
      <div class="flex-row">
        <img src="/instagram/thumb-card3N.png" alt="instaPosts">
        <img src="/instagram/thumb-card4N.png" alt="instaPosts">
        <img src="/instagram/thumb-card5N.png" alt="instaPosts">
      </div>
      <div class="flex-rowe">
        <img src="/instagram/thumb-card6N.png" alt="instaPosts">
        <img src="/instagram/thumb-card7.png" alt="instaPosts">
        <img src="/instagram/thumb-card8.png" alt="instaPosts">
      </div>
    </div>
    <div class="follow" data-aos="fade-left" data-aos-delay="200">
      <h2>Follow us</h2>
      <p>Let us be social</p>
      <div>
        <i class="fab fa-facebook"></i>
        <i class="fab fa-instagram"></i>
        <i class="fab fa-twitter"></i>
        <i class="fab fa-youtube"></i>
      </div>
    </div>
  </div>
  <div class="rights flex-rowe">
    <h4 class="text-gray">
      Copyrights Reserved &copy;
      <a href="#" target="_blank">Kapil Chandna</a>
    </h4>
  </div>
  <div class="move-up" @click="scrollToTop">
    <span>
      <i class="fas fa-arrow-circle-up fa-2x"></i>
    </span>
  </div>
</footer>
</template>
<script>
export default {
  name: 'app-footer',
  methods: {
    scrollToTop () {
      window.scrollTo(0,0)
    }
  }
  
};
</script>
<style>
footer.footere {
  height: 100%;
  background: #0f0f0f;
  position: relative;
}

footer.footere .containere {
  display: grid;
  grid-template-columns: repeat(4,1fr);
}

footer .containere .about-us button {
  background: black;
}
footer.footere .containere > div {
  flex-grow: 1;
  flex-basis: 0;
  padding: 3rem 0.9rem;
}

footer.footere .containere h2 {
  color: white;
}

footer.footere .newsletter .form-element {
  background: black;
  display: inline-block;
  width: 100%;
}

footer.footere .newsletter .form-element input {
  padding: 0.5rem 0.7rem;
  border: none;
  background: transparent;
  color: white;
  font-family: var(--Jose);
  font-size: 1rem;
  width: 88%;
}

footer.footere .newsletter .form-element span {
  background: var(--sky);
  padding: 0.5rem 0.7rem;
  cursor: pointer;
}

footer.footere .instagram div > img {
  display: inline-block;
  width: 25%;
  height: 50%;
  padding: 0.3rem 0.4rem;
}

footer.footere .follow div i {
  color: white;
  padding: 0 0.4rem;
}

footer.footere .rights {
  justify-content: center;
  font-family: var(--Jose);
}

footer.footere .rights h4 a {
  color: white;
}

footer.footere .move-up {
  position: absolute;
  right: 6%;
  top: 50%;
}

footer.footere .move-up span {
  color: var(--midnight);
}

footer.footere .move-up span:hover {
  color: white;
  cursor: pointer;
}


@media only screen and (max-width: 1130px) {
  footer.footere .containere {
    grid-template-columns: repeat(2, 1fr);
  }
}

/*Viewport less than or equal to 750px*/

@media only screen and (max-width: 750px) {
  footer.footere .containere {
    grid-template-columns: repeat(1, 1fr);
  }
}

/*Viewport less than or equal to 520px*/

@media only screen and (max-width: 520px){
  footer.footere .containere > div {
    padding: 1rem 0.9rem !important;
  }

  footer.footere .newsletter .form-element input {
    width: 74%;
  }   

  footer .rights {
    padding: 0 1.4rem;
    text-align: center;
  }
}

</style>
