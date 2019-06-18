<template>
  <div class="container_1">
    <Nav/>
    <Contact/>
    <Footer />
  </div>
</template>

<script>
import { mapActions } from 'vuex';
import { mapGetters } from 'vuex';

import Nav from "../components/Nav";
import Contact from "../components/Contact";
import Footer from "../components/Footer";

export default {
  name: "ContactPage",
  components: {
    Nav,
    Contact,
    Footer
  },
  computed: mapGetters(['totalNews', 'selectedNews']),
  methods: mapActions(['init']),
  created() {
    this.init();
  }
};
</script>

<style lang="postcss">
@import "../styles/base/_variables.css";
@import "../styles/base/_global.css";
</style>

