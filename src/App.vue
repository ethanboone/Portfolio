<template>
  <main class="flex-column">
    <div class="container-fluid">
      <div class="row bg-navbar justify-content-center">
        <div class="col-12 col-md-10 d-flex justify-content-center">
          <ul class="nav nav-tabs">
            <li class="nav-item" href="#">
              <router-link :to="{ name: 'Home' }" class="nav-link">
                <a href="#" class="text-light">Home</a>
              </router-link>
            </li>
            <li class="nav-item" href="#">
              <router-link :to="{ name: 'Projects' }" class="nav-link">
                <a class="text-light">Projects</a>
              </router-link>
            </li>
            <li class="nav-item" href="#">
              <router-link :to="{ name: 'Contact' }" class="nav-link">
                <a class="text-light">Contact</a>
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div id="app" class="container-fluid">
      <router-view />
    </div>
  </main>
  <footer>
    <div class="bg-navbar text-light text-center p-4">
      Made by Ethan Boone
    </div>
  </footer>
</template>

<script>
import { computed } from 'vue'
import { AppState } from './AppState'
export default {
  name: 'App',
  setup() {
    return {
      appState: computed(() => AppState)
    }
  }
}
</script>
<style lang="scss">
@import "./assets/scss/main.scss";
.dropdown-menu {
  user-select: none;
  display: block;
  transform: scale(0);
  transition: all 0.15s linear;
}
.dropdown-menu.show {
  transform: scale(1);
}
.hoverable {
  cursor: pointer;
}
a:hover {
  text-decoration: none;
}
.nav-link{
  text-transform: uppercase;
}
.nav-item .nav-link.router-link-exact-active{
  color: var(--secondary);
}

.bg-navbar {
  background-color: var(--dark);
}

#app {
  background-image: url("./assets/img/portfolio.jpg");
  background-size: cover;
}

img{
  filter: grayscale(100%);
}
</style>
