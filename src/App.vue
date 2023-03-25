<template>
  <navbar
    :pages="pages"
    :active-page="activePage"
    :nav-link-click="(index) => activePage = index"
    >
  </navbar>
  <page-viewer
    :page="pages[activePage]">
  </page-viewer>
</template>

<script>
import PageViewer from './components/PageViewer.vue';
import Navbar from './components/Navbar.vue';

export default {
    components:{
        Navbar,
        PageViewer
    },
        data() {
                return {
                    activePage: 0,
                    theme: 'dark',
                    pages: [
                        {
                            link: {text: "Home", url: 'index.html'},
                            pageTitle: 'Home page!',
                            paragraph: 'This is the Home page of Vue'
                        },
                        {
                            link: {text: "About", url: 'about.html'},
                            pageTitle: 'About page!',
                            paragraph: 'This is the About Page of Vue'
                        },
                        {
                            link: {text: "Contact", url: 'contact.html'},
                            pageTitle: 'Contact page!',
                            paragraph: 'This is the Contact Page'
                        }
                    ],
                };
            },

}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
