<template>
  <div class="app">
    <header class="row center nav">
      <div class="container-img center-total">
          <img id="header-memoji" src="@/assets/memoji/memoji_1.png" alt="memoji">
      </div>
      <div v-show="!mobile" class="row buttons">
        <router-link v-for="link in links" :key="link.id" @click="changeStatut(link.id)" class="button-nav center-total" :class="{active: link.active}" :to="link.name">
          {{ link.name }}
        </router-link>
      </div>
      <div class="burger">
        <img @click="openMobileMenu" v-show="mobile" :class="{ 'menu-active' : mobileNav }" src="@/assets/menu-burger.png" alt="menu">
      </div>
      <transition>
        <div v-show="mobileNav" class="mb-nav column">
          <router-link v-for="link in links" :key="link.id" @click="changeStatut(link.id)" class="button-nav center-total" :class="{active: link.active}" :to="link.name">
            {{ link.name }}
          </router-link>
        </div>
      </transition>
    </header>
    <Home  v-if="activePage == 0"/>
    <Skills v-if="activePage == 1" />
    <Projects v-if="activePage == 2" />
    <Experience v-if="activePage == 3" />
    <Contact v-if="activePage == 4"/>
  </div>
  <MainFooter />
</template>

<script>
import Home from './components/Home.vue'
import MainFooter from './components/MainFooter.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
import Experience from './components/Experience.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: { Home,MainFooter,Skills,Projects,Experience,Contact },
  data() {
    return {
        scrolledNav: null,
        mobile: null,
        mobileNav: null,
        windowWidth: null,

        links: [
          { id: 0, path:"/", name: "Home", active: true },
          { id: 1, path:"/skills", name: "Skills", active: false },
          { id: 2, path:"/projects", name: "Projects", active: false },
          { id: 3, path:"/experience", name: "Experience", active: false },
          { id: 4, path:"/contact", name: "Contact", active: false },
        ],
        activePage: 0,
    };
  },
  created() {
    window.addEventListener('resize', this.checkScreen)
    this.checkScreen()
  },

  methods: {
    changeStatut(id) {
      this.links.forEach(route => {
        if (route.id === id) {
          route.active = true
          this.activePage = id
        } else {
          route.active = false
        }
      });
    },
    openMobileMenu() {
      this.mobileNav = !this.mobileNav
    },
    checkScreen() {
      this.windowWidth = window.innerWidth
      if (this.windowWidth <= 750) {
        this.mobile = true
        return
      }
      this.mobile = false
      this.mobileNav = false
      return
    },
  },
}

</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');
  * {
    font-family: "Inter";
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    list-style: none;
    text-decoration: none;
    color: var(--black);
    font-size: 18px;
  }
  h2 {
    font-size: 36px;
  }
  :root {
    --gradient: linear-gradient(180.82deg, #000000 13.95%, #506CB5 88.12%);
    --blue: #506CB5;
    --black: #000;
    --grey: #A6A6A6;
    --white: #F3F3F3;
    --bgApp: #EFEFEF;
    --bgFooter: #4D4D4D;
    --bgContainer: #F9F9F9;
  }
  .app {
    z-index: 1;
    position: relative;
    width: 100%;
    background-color: var(--bgApp);
    -webkit-font-smoothing: antialiased;
    margin-bottom: 200px;
  }
  .arrow {
    width: 20px;
    height: 20px;
    margin-bottom: 15px;
  }
  .button {
    margin: 0 auto;
    padding: 1rem;
    width: fit-content;
    border-radius: 30px;
    box-shadow: 0px 2px 8px 0px #00000040;
    a,p {
      font-size: 14px;
    }
    &:hover {
        transition: ease 0.3s;
        transform: scale(1.05);
        a {
          color: var(--blue);
        }
    }
  }
  .active {
    color: var(--white);
    font-weight: bold;
    background-color: var(--blue);
    box-shadow: 0px 2px 8px 0px #00000040;
  }
  .gradient {
    background: var(--gradient);
    background-clip: text;
    color: transparent;
    font-weight: normal;
  }
  .center-total {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .flex-wrap {
    display: flex;
    flex-wrap: wrap;
  }
  .column {
    display: flex;
    flex-direction: column;
  }
  .burger {
    position: absolute;
    top: 0;
    right: 0;
    padding: 1rem;
    cursor: pointer;
    img {
      width: 30px;
      height: 30px;
    }
  }
  .menu-active {
    transition: ease 0.3s all;
    transform: rotate(-90deg);
  }
  .mb-nav {
    width: 100%;
    bottom: 0;
    position: fixed;
    z-index: 1;
    background-color: var(--bgFooter);
    router-link {
      padding: 2rem;
      font-size: 18px;
      width: 100%;
      border-radius: 0;
      color: var(--white);
    }
  }
  .nav {
    padding: 2rem;
    justify-content: center;
    justify-content: space-evenly;
  }
  .buttons {
    padding: 0.5rem;
    height: 50px;
    border-radius: 30px;
    align-items: center;
    justify-content: center;
    background-color: var(--bgContainer);
  }
  .button-nav {
    cursor: pointer;
    width: 90px;
    height: 40px;
    border-radius: 30px;
    font-size: 12px;
  }
  .button-contact {
    width: 95px;
    height: 50px;
    border-radius: 30px;
    background-color: var(--bgContainer);
    &:hover {
        transition: ease 0.3s;
        color: var(--white);
        font-weight: bold;
        background-color: var(--blue);
    }
  }
  .container-img {
    border-radius: 50%;
    width: 50px;
    height: 50px;
    background-color: var(--bgContainer);
    box-shadow: 0px 2px 8px 0px #00000040;
    #header-memoji {
        width: 36px;
        height: 46px;
    }
  }
  @media screen and (max-width: 750px) {
    .nav {
      padding: 0;
      justify-content: unset;
      margin-bottom: 80px;
    }
    .container-img {
      position: fixed;
      top: 1%;
      left: 2%;
    }
  }
</style>
