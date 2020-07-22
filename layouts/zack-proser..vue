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

</style>