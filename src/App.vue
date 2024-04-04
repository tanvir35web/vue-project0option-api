<template>
  <Navbar
    :useDarkNavBar="useDarkNavBar"
    :pages="pages"
    :activePage="activePage"
    @toggle-theme="toggleNavBarTheme"
    :navLinkClick="(index) => (activePage = index)"
  />
  <PageViewer :page="pages[activePage]" />
</template>

<script>
import PageViewer from './components/PageViewer.vue'
import Navbar from './components/Navbar.vue'

export default {
  components: {
    Navbar,
    PageViewer
  },

  data() {
    return {
      activePage: 0,
      useDarkNavBar: false,
      pages: [
        {
          link: { text: 'Home', url: 'index.html' },
          pageTitle: 'Home Page',
          content: 'This is the home content'
        },
        {
          link: { text: 'About', url: 'about.html' },
          pageTitle: 'About Page',
          content: 'This is the about content'
        },
        {
          link: { text: 'Contact', url: 'contact.html' },
          pageTitle: 'Contact Page',
          content: 'This is the contact content'
        }
      ]
    }
  },
  methods: {
    toggleNavBarTheme() {
      this.useDarkNavBar = !this.useDarkNavBar;
    }
  }
}
</script>
