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
    </div>
  </header>
</template>

<script>
// import blockBuer from './blockBuer.vue';
// import blockAboutUs from './blockAboutUs.vue';
// import blockRegMail from './blockRegMail.vue';

export default {
  name: "headerComp",
  props: {
    msg: String,
  },
  components: {
    // blockBuer,
    // blockAboutUs,
    // blockRegMail,
  },
  data() {
    return {
      showNavbar: true,
      lastScrollPosition: 0,
      // scrollValue: 0,
    };
  },

  mounted() {
    this.lastScrollPosition = window.pageYOffset;
    window.addEventListener("scroll", this.onScroll);
    // const viewportMeta = document.createElement("meta");
    // viewportMeta.name = "viewport";
    // viewportMeta.content = "width=device-width, initial-scale=1";
    // document.head.appendChild(viewportMeta);
  },

  beforeDestroy() {
    window.removeEventListener("scroll", this.onScroll);
  },

  methods: {
    OFFSET: 40,
    onScroll() {
      if (window.pageYOffset < 0) {
        return;
      }
      if (Math.abs(window.pageYOffset - this.lastScrollPosition) < 40) {
        return;
      }
      this.showNavbar = window.pageYOffset < this.lastScrollPosition;
      this.lastScrollPosition = window.pageYOffset;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.headerComp {
  // background-color: #acacac;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 50;
  // width: 1390px;
  // z-index: 1000;
}

.header-container {
  background-color: #acacac;
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
  // margin-left: 5px;
}
.icon {
  margin-right: 25px;
}

.icon:nth-last-child(1) {
  margin-right: 0px;
}
</style>
