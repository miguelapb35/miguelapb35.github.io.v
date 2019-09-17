<template>
  <div class="wrapper">
    <parallax class="page-header header-filter" :style="headerStyle">
      <div class="md-layout">
        <div class="md-layout-item">
          <div class="image-wrapper">
            <div class="brand">
              <h1>Visos Beauty Salon</h1>
              <h3>W Hair, M Hair, EyeBrows, Eyelashes</h3>
            </div>
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">




      
 <!--      <div class="tabla">
        <md-table md-card>
          <md-table-toolbar>
            <h1 class="ti">Services</h1>
          </md-table-toolbar>

          <md-table-row>
            <md-table-head>Service</md-table-head>
            <md-table-head>Price</md-table-head>
          </md-table-row>

          <md-table-row>
            <md-table-cell>Kids hair cut</md-table-cell>
            <md-table-cell md-numeric  class="list-item">$ 12 and up</md-table-cell>
          </md-table-row>

          <md-table-row>            
            <md-table-cell>Mens hair cut</md-table-cell>
            <md-table-cell md-numeric>$ 14 and up</md-table-cell>
          </md-table-row>

          <md-table-row>            
            <md-table-cell>Women hair cut</md-table-cell>
            <md-table-cell md-numeric>$ 16 and up</md-table-cell>
          </md-table-row>

          <md-table-row>            
            <md-table-cell>Women color</md-table-cell>
            <md-table-cell md-numeric>$ 58 and up</md-table-cell>
          </md-table-row>

          <md-table-row>
            <md-table-cell>Women high light</md-table-cell>
            <md-table-cell md-numeric>$ 55 and up</md-table-cell>
          </md-table-row>  

          <md-table-row>
            <md-table-cell>Face Waxing of eye brows</md-table-cell>
            <md-table-cell md-numeric>$ 10</md-table-cell>
          </md-table-row>  

          <md-table-row>
            <md-table-cell>Lip</md-table-cell>
            <md-table-cell md-numeric>$ 8</md-table-cell>
          </md-table-row> 

          <md-table-row>
            <md-table-cell>Eye brows & lip</md-table-cell>
            <md-table-cell md-numeric>$ 15</md-table-cell>
          </md-table-row> 
            
          <md-table-row>
            <md-table-cell>Total face</md-table-cell>
            <md-table-cell md-numeric>$ 45</md-table-cell>
          </md-table-row>   
          
          <md-table-row>
            <md-table-cell>Body waxing : Armpits</md-table-cell>
            <md-table-cell md-numeric>$ 20 and up</md-table-cell>
          </md-table-row>  

          <md-table-row>
            <md-table-cell>Bikini</md-table-cell>
            <md-table-cell md-numeric>$ 20 and up</md-table-cell>
          </md-table-row>          

          <md-table-row>
            <md-table-cell>Legs</md-table-cell>
            <md-table-cell md-numeric>$ 50</md-table-cell>
          </md-table-row> 

          <md-table-row>
            <md-table-cell>Half Legs</md-table-cell>
            <md-table-cell md-numeric>$ 25</md-table-cell>
          </md-table-row> 
          <md-table-row>
            <md-table-cell>Feet</md-table-cell>
            <md-table-cell md-numeric>$ 15</md-table-cell>
          </md-table-row> 
          <md-table-row>
            <md-table-cell>Make up</md-table-cell>
            <md-table-cell md-numeric>$ 30</md-table-cell>
          </md-table-row> 
          <md-table-row>
            <md-table-cell>Eyelash</md-table-cell>
            <md-table-cell md-numeric>$ 15</md-table-cell>
          </md-table-row> 

        </md-table>
      </div> -->
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
      default: require("@/assets/img/headerabout.jpg")
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
    }
  },
};
</script>
<style lang="scss">
.section-download {
  .md-button + .md-button {
    margin-left: 5px;
  }
}
.ti {
  color: #6d6b6b;
}
.tabla{
  width: 90%;
  margin-left: 30px;
}

.list-item {
    display: inline-block;
    margin-right: 10px;
    transition: all 1s;
    transform: opacity(0.5);    
}

.list-enter-active, .list-leave-active {
    transition: all 1s;
}

.list-enter, .list-leave-to {
    opacity: 0;
    transform: translateY(30px);
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
