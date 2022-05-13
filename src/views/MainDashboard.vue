<template>
  <div class="wrapper">
    <parallax class="page-header header-filter" :style="headerStyle">
      <div class="md-layout">
        <div class="md-layout-item">
          <div class="image-wrapper">
            <img :src="leaf4" alt="leaf4" class="leaf4" v-show="leafShow" />
            <img :src="leaf3" alt="leaf3" class="leaf3" v-show="leafShow" />
            <img :src="leaf2" alt="leaf2" class="leaf2" v-show="leafShow" />
            <img :src="leaf1" alt="leaf1" class="leaf1" v-show="leafShow" />
            <div class="brand">
              <h1>Vue Material Kit</h1>
              <h3>A Badass Vue.js UI Kit made with Material Design.</h3>
            </div>
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">
      <div class="md-layout">
        <div class="md-layout-item text-center">
          <md-button href="#/login" class="md-simple md-success md-lg"
            >View Login Page</md-button
          >
        </div>
      </div>
      <div class="section section-examples">
        <span>section examples</span>
      </div>
      <div class="section section-download" id="downloadSection">
        <div class="container">
          <div class="md-layout text-center">
            <span>layout text-center</span>
          </div>
          <br /><br />

          <div class="md-layout text-center">
            <span>layout text-center</span>
            </div>
          <div class="sharing-area text-center">
            <div class="md-layout">
              <div class="md-layout-item">
                <h3>Thank you for supporting us!</h3>
              </div>
            </div>

            <md-button class="md-twitter"
              ><i class="fab fa-twitter"></i>Tweet</md-button
            >
            <md-button class="md-facebook"
              ><i class="fab fa-facebook-square"></i> Share</md-button
            >
            <md-button class="md-google"
              ><i class="fab fa-google-plus"></i> Share</md-button
            >
            <md-button class="md-github"
              ><i class="fab fa-github"></i> Star</md-button
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Parallax from '@/components/Parallax.vue'
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'MainDashboard',
  bodyClass: 'index-page',
  components: {
    Parallax
  },
  props: {
    image: {
      type: String,
      default: require("@/assets/img/vue-mk-header.jpg")
    },
    leaf4: {
      type: String,
      default: require("@/assets/img/leaf4.png")
    },
    leaf3: {
      type: String,
      default: require("@/assets/img/leaf3.png")
    },
    leaf2: {
      type: String,
      default: require("@/assets/img/leaf2.png")
    },
    leaf1: {
      type: String,
      default: require("@/assets/img/leaf1.png")
    }
  },

  data() {
    return {
      leafShow: false
    }
  },

  methods: {
    leafActive() {
      if (window.innerWidth < 768) {
        this.leafShow = false
      } else {
        this.leafShow = true
      }
    }
  },

  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.image})`
      }
    }
  },

  mounted() {
    this.leafActive()
    window.addEventListener('resize', this.leafActive)
  },

  beforeDestroy() {
    window.removeEventListener('resize', this.leafActive)
  }
  
}
</script>

<style>
 
</style>