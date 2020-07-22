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

html, body {
  margin: 0%;
  box-sizing: border-box;
  overflow-x: hidden;
  scroll-behavior: smooth;
}

:root {

/*  Color Schemes*/
  --text-gray: #3f4954;
  --text-light: #686666da;
  --bg-color: #0f0f0f;
  --midnight: #104f55;

/*  gradient-color : webgradients.com*/
  --sky: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%);

}

a {
  text-decoration: none;
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
  font-family: 'Lexend', cursive;
  font-size: 2.5rem;
}

h3 {
  font-family: 'Abel', cursive;
  font-size: 1.3rem;
}

h2 {
  font-family: 'Lexend', cursive;
}

.btn {
  border: none;
  border-radius: 2rem;
  padding: 1rem 3rem;
  font-size: 1rem;
  font-family: 'Livvic', cursive;
  cursor: pointer;
  outline: none;
}

span {
  font-family: 'Abel', cursive;
}

p {
  font-family: 'Lexend', cursive;
  color: var(--text-light);
}
.containere {
  margin: 0 5vw;
}

.text-gray {
  color: var(--text-gray);
}


</style>