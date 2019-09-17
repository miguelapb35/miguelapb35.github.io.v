<template>
  <div class="wrapper">
    <parallax class="page-header header-filter" :style="headerStyle">
      <div class="md-layout">
        <div class="md-layout-item">
          <div class="image-wrapper">
            <div class="brand">
              <h1>Come Visit Us</h1>
            </div>
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">
      <div class="section section-contacts">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-66 md-xsmall-size-100 mx-auto">
              <h2 class="text-center title">For Appointments</h2>
              <h2 class="text-center title">303 693 3089</h2>
              <h2 class="text-center title">303 693 0422</h2>
              <h3 class="text-center title">15433A E. Hampden Av. Aurora, Co, 80013</h3>
                      <div class="mx-auto text-center">
                        <img src="../assets/img/visos-salon.jpeg" alt="salon" class="salon">
                      </div>
                  <div class="tabla">
                    <md-table md-card>
                      <md-table-toolbar>
                        <h2 class="ti">Hours of Operation</h2>
                      </md-table-toolbar>

                      <md-table-row>
                        <md-table-head>Day</md-table-head>
                        <md-table-head>Hours</md-table-head>
                      </md-table-row>

                      <md-table-row>
                        <md-table-cell>Monday</md-table-cell>
                        <md-table-cell md-numeric>9:30 am -7 pm</md-table-cell>
                      </md-table-row>
                      <md-table-row>
                        <md-table-cell>Tuesday</md-table-cell>
                        <md-table-cell md-numeric>9:30 am -7 pm</md-table-cell>
                      </md-table-row>
                      <md-table-row>
                        <md-table-cell>Wednesday</md-table-cell>
                        <md-table-cell md-numeric>9:30 am -7 pm</md-table-cell>
                      </md-table-row>
                      <md-table-row>
                        <md-table-cell>Thursday</md-table-cell>
                        <md-table-cell md-numeric>9:30 am -7 pm</md-table-cell>
                      </md-table-row>
                      <md-table-row>
                        <md-table-cell>Friday</md-table-cell>
                        <md-table-cell md-numeric>9:30 am -7 pm</md-table-cell>
                      </md-table-row>
                      <md-table-row>
                        <md-table-cell>Saturday</md-table-cell>
                        <md-table-cell md-numeric>9:00 am -7 pm</md-table-cell>
                      </md-table-row>
                      <md-table-row>
                        <md-table-cell>Sunday</md-table-cell>
                        <md-table-cell md-numeric>Closed</md-table-cell>
                      </md-table-row>
                    </md-table>
                  </div> 
                  <div class="mx-auto text-center">   
                    <img src="../assets/img/visos-salon3.jpeg" alt="salon" class="text-center salon">  
                  </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navigation from "./components/NavigationSection";
import SmallNavigation from "./components/SmallNavigationSection";

export default {
  components: {
    Navigation,
    SmallNavigation,
  },
  name: "index",
  bodyClass: "index-page",
  props: {
    image: {
      type: String,
      default: require("@/assets/img/vue-mk-header.jpg")
    }
  },
  data() {
    return {
      firstname: null,
      email: null,
      password: null,
      leafShow: false
    };
  },
  methods: {
    leafActive() {
      if (window.innerWidth < 768) {
        this.leafShow = false;
      } else {
        this.leafShow = true;
      }
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.image})`
      };
    },
    signupImage() {
      return {
        backgroundImage: `url(${this.signup})`
      };
    }
  },
  mounted() {
    this.leafActive();
    window.addEventListener("resize", this.leafActive);
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.leafActive);
  }
};
</script>
<style lang="scss">
.section-download {
  .md-button + .md-button {
    margin-left: 5px;
  }
}
.salon {
  width: 100%;
  max-width: 440px;
}
.ti {
  color: #6d6b6b;
}
  .tabla{
    width: 90%;
    margin-left: 10px;
  }

@media all and (min-width: 991px) {
  .btn-container {
    display: flex;
  }
  .md-title {
    color: Black;
  }
  .ti {
    color: #6d6b6b;
  }
  .tabla{
    width: 90%;
  }
}
</style>
