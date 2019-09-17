<template>
  <div class="wrapper">
    <parallax class="page-header header-filter" :style="headerStyle">
      <div class="md-layout">
        <div class="md-layout-item">
          <div class="image-wrapper">
            <div class="brand">
              <h1>Visos Beauty Salon</h1>
              <!-- <h3>W Hair, M Hair, EyeBrows, Eyelashes</h3> -->
              <h4>
                303 693 3089, 303 693 0422
              </h4>
              <p>
                15433A E. Hampden Av. Aurora, Co, 80013
              </p>
            </div>
          </div>
        </div>
      </div>
    </parallax>
    <div class="main main-raised">
      <div class="tabla">
        <md-table md-card>
          <md-table-toolbar>
            <h1 class="ti">Services</h1>
          </md-table-toolbar>
          <div id="staggered-list-demo">

                  <input v-model="query" class="searchbox" placeholder="Type service here...">
            
            <transition-group
              name="staggered-fade"
              tag="ul"
              v-bind:css="false"
              v-on:before-enter="beforeEnter"
              v-on:enter="enter"
              v-on:leave="leave"
            >
              <md-table-row 
                v-for="(item, index) in computedList"
                v-bind:key="item.Service"
                v-bind:price="item.Price"
                v-bind:data-index="index" 
              >
                    
                      <md-table-cell class="itemService">{{ item.Service }}</md-table-cell>      
                      <div class="price">
                        <md-table-cell md-numeric class="list-item der itemPrice">{{ item.Price }}</md-table-cell>
                      </div>
                      
                              
              </md-table-row>
            </transition-group>          
          </div>
        </md-table>
      </div> 
    </div>
  </div>
</template>

<script>
import Navigation from "./components/NavigationSection";
import SmallNavigation from "./components/SmallNavigationSection";
import { setTimeout } from 'timers';

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
      /* default: require("@/assets/img/headerabout.jpg") */
      default: require("@/assets/img/vue-mk-header.jpg")
    }
  },
  data() {
    return {
      firstname: null,
      email: null,
      password: null,
      leafShow: false,
      query: '',
      list: [
            { Service: 'Kids hair cut', Price: '$ 12 and up'  },
            { Service: 'Mens hair cut', Price: '$ 14 and up' },
            { Service: 'Women hair cut', Price: '$ 16 and up' },
            { Service: 'Women color', Price : '$ 58 and up' },
            { Service: 'Women high light', Price: '$ 55 and up' },        
            { Service: 'Face Waxing of eye brows', Price: '$ 10' },        
            { Service: 'Lip', Price: '$ 8' },        
            { Service: 'Eye brows & lip', Price: '$ 15' },        
            { Service: 'Total face', Price: '$ 45' },        
            { Service: 'Body waxing : Armpits', Price: '$ 20 and up' },        
            { Service: 'Bikini', Price: '$ 20 and up' },        
            { Service: 'Legs', Price: '$ 50' },        
            { Service: 'Half Legs', Price: '$ 25' },        
            { Service: 'Feet', Price: '$ 15' },        
            { Service: 'Make up', Price: '$ 30' },        
            { Service: 'Eyelash', Price: '$ 15' },        
                    
      ]
    };
  },
  methods: {
    beforeEnter: function (el) {
      el.style.opacity = 0
      el.style.height = 0
    },
    enter: function (el, done) {
      var delay = el.dataset.index * 150
      setTimeout(function () {
        Velocity(
          el,
          { opacity: 1, height: '1.6em' },
          { complete: done }
        )
      }, delay)
    },
    leave: function (el, done) {
      var delay = el.dataset.index * 150
      setTimeout(function () {
        Velocity(
          el,
          { opacity: 0, height: 0 },
          { complete: done }
        )
      }, delay)
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.image})`
      };
    },
    computedList: function () {
      var vm = this
      return this.list.filter(function (item) {
        return item.Service.toLowerCase().indexOf(vm.query.toLowerCase()) !== -1
      })
    }
  },
};
</script>
<style lang="scss">
@media all and (max-width: 450px) {
.brand h1 {
  font-size: 1.5em;
}
h1 {
  font-size: 1.2em;
}
} 

.brand h1 {
  font-size: 3.5em;
}
.price {
  justify-content: right;
  margin-right: 0;
}

#staggered-list-demo {
  justify-content: center;
  display: grid;
}
.md-table-cell-container {
  justify-content: right;
}
.searchbox {
  justify-content: center;
  border-radius: 5px;
  margin-inline-start: 40px;
  opacity: 0.9;
  line-height: 24px;
}

.md-table-cell {
  height: 48px;
  position: relative;
  transition: .3s cubic-bezier(.4,0,.2,1);
  line-height: 18px;
}
.md-table-cell-container {
  font-size: 0.7rem;
}
li  {
  list-style-type: none;
  margin-bottom: inherit;
}
.section-download {
  .md-button + .md-button {
    margin-left: 5px;
  }
}
.ti {
  color: #6d6b6b;
}
.tabla {
  width: 90%;
  margin-left: 10px;
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
  td {
    border-color: transparent;
  }

@media all and (min-width: 768px) {
.md-table-cell-container {
  font-size: 1.5rem;
  
}
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
td {
  border-color: transparent;
}
  .tabla{
    width: 90%;
  }
  .md-table-cell-container {
  font-size: 1.5rem;
  
}
}
</style>
