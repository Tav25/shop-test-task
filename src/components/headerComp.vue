<template>
  <header class="headerComp">
    <div
      class="header-container _container"
      :class="{ 'hidden-header-container': !showNavbar }"
    >
      <!-- <blockBuer />
    <blockAboutUs />
    <blockRegMail /> -->
      <div class="logo">LOGO</div>
      <div class="icons">
        <ul>
          <li class="icon">
            <img src="../assets/icons/person.svg" alt="icon" />
          </li>
          <li class="icon">
            <img src="../assets/icons/favorite.svg" alt="icon" />
          </li>
          <li class="icon">
            <img src="../assets/icons/Group.svg" alt="icon" />
          </li>
        </ul>
      </div>
      <burgerComp class="burger-icon"></burgerComp>
    </div>
  </header>
</template>

<script>
import burgerComp from "./Ui/burgerComp.vue";
// import blockAboutUs from './blockAboutUs.vue';
// import blockRegMail from './blockRegMail.vue';

export default {
  name: "headerComp",

  components: {
    burgerComp,
  },
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0,
    };
  },

  mounted() {
    this.lastScrollPosition = window.pageYOffset;
    window.addEventListener("scroll", this.onScroll);
  },

  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },

  methods: {
    headerHeight: 40,
    onScroll() {
      if (window.pageYOffset < 0) {
        return;
      }
      if (Math.abs(window.pageYOffset - this.lastScrollPosition) < this.headerHeight) {
        return;
      }
      this.showNavbar = window.pageYOffset < this.lastScrollPosition;
      this.lastScrollPosition = window.pageYOffset;
    },
  },
};
</script>

<style scoped lang="scss">
.headerComp {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 50;
}

.header-container {
  background-color: #ffffff;
  min-height: 40px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  transition: 0.25s;
}
.header-container.hidden-header-container {
  opacity: 0;
  transition: 0.25s;
}

li {
  display: inline-block;
}

.logo {
  font-weight: 700;
  font-size: 22px;
  line-height: 72%;
  letter-spacing: 0.04em;
  text-transform: uppercase;

  color: #000000;
}

.icons {
  flex: 1 1 auto;
  text-align: right;
}
.icon {
  margin-right: 25px;
}

.icon:nth-last-child(1) {
  margin-right: 0px;
}

.burger-icon {
  display: none;
}

@media only screen and (max-width: 768px) {
  .icon:nth-last-child(1) {
    margin-right: 25px;
  }

  .burger-icon {
    display: flex;
  }
}
</style>
