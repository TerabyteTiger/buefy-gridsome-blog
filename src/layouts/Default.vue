<template>
  <div>
    <section class="section">
      <div class="container">
        <div class="columns is-multiline is-desktop">
          <div class="column is-one-quarter is-narrow">
            <AuthorCard />
          </div>
          <div class="column">
            <slot />
          </div>
        </div>
      </div>
    </section>
    <Footer />
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import AuthorCard from "~/components/AuthorCard.vue";
import Footer from "~/components/Footer.vue";
export default {
  components: {
    AuthorCard,
    Footer,
  },
};
</script>

<style>
  #app {
    min-height: 100vh;
    display: flex; 
    flex-direction: column;
    justify-content: space-between;
  }
</style>