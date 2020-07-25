<template>
    <div id="wrapper" class="d-flex flex-column">
        <header class="header-global">
            <app-header></app-header>
        </header>
        <main class="flex-fill position-relative">
           <nuxt />
        </main>
        <footer class="footer-global">
          <app-footer></app-footer>
        </footer>
    </div>
</template>

<script>
import AppHeader from "~/components/zack-proser/AppHeader";
import AppFooter from "~/components/zack-proser/AppFooter";

export default {
  components: {
    AppHeader,
    AppFooter
  }
};
</script>
<style>
@import "~/assets/fonts.css";

html, body {
  margin: 0%;
  box-sizing: border-box;
  overflow-x: hidden;
  scroll-behavior: smooth;
}

:root {

/*  Fonts */
  --Abel:'Abel',cursive;
  --Liv: 'Livvic',cursive;
  --Lex: 'Lexend',cursive;

/*  Color Schemes*/
  --text-gray: #3f4954;
  --text-light: #686666da;
  --bg-color: #0f0f0f;
  --midnight: #104f55;

/*  gradient-color : webgradients.com*/
  --sky: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);

}

a {
  text-decoration: none !important;
  color: var(--text-gray);
}


.flex-rowe
 {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

ul {
  list-style-type: none;
}

h1 {
  font-family: var(--Lex)  !important;
  font-size: 2.5rem  !important;
}

h3 {
  font-family: var(--Abel)  !important;
  font-size: 1.3rem  !important;
}

h2 {
  font-family: var(--Lex)  !important;
  font-size: 1.7rem  !important;
}

h4{
  font-size: 1rem  !important;
}

.btn {
  border: none;
  border-radius: 2rem;
  padding: 1rem 3rem;
  font-size: 1rem  !important;
  font-family: var(--Liv);
  cursor: pointer  !important;
  outline: none  !important;
}

span {
  font-family: var(--Abel)  !important;
}

p {
  font-family: var(--Lex)  !important;
  color: var(--text-light)  !important;
}
.containere {
  margin: 0 5vw;
}

.text-gray {
  color: var(--text-gray);
}


</style>