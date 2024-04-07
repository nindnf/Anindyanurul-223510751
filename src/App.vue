<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/ft2.jpeg" width="400" height="480" />

    <div class="wrapper">
      <HelloWorld msg="WELCOME TO CV WEB!" />  
      <nav>
        <RouterLink to="/">
          <button class="nav-button">Home</button>
        </RouterLink>
        <RouterLink to="/about">
          <button class="nav-button">About</button>
        </RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 11px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav button.nav-button {
  display: inline-block;
  padding: 0.5rem 1rem;
  margin: 0 0.5rem;
  border: none;
  border-radius: 4px;
  background-color: var(--color-primary); 
  color: black;
  font-size: 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

nav button.nav-button:hover {
  background-color: var(--color-primary-dark);
}

nav button.nav-button:first-of-type {
  margin-left: 0;
}

nav button.nav-button:last-of-type {
  margin-right: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;
    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
