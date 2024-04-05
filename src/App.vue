<template>
    <div class="container">
      <HeaderLayout />
      <router-view/>
      <FooterLayout />
    </div>
</template>

<script>
import HeaderLayout from "@/components/HeaderLayout.vue";
import FooterLayout from "@/components/FooterLayout.vue";

export default {
  name: 'App',
  components: {
    FooterLayout,
    HeaderLayout,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

#app {
  color: #2c3e50;
}

html {
  background-color: #191b1f;
  line-height: 1.5;
  font-family: 'Inter', ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, Noto Sans, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
}

body {
  margin: 0;
}

a {
  color: rgba(255,255,255);
  transition: color .2s ease-in-out;
}

a, p {
  font-size: 16px;
}

h1 {
  line-height: 2.5rem;
}

a:hover {
  cursor: pointer;
  opacity: 1 !important;
}
</style>
