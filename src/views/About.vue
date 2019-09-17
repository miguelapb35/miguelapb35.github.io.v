<template>
  <div class="wrapper">
    <parallax
      class="section page-header header-filter"
      :style="headerStyle"
    >
      <div class="container">
        <div class="md-layout">
          <div class="md-layout-item"></div>
          <div class="md-layout-item"></div>
          <div class="md-layout-item md-size-50 md-small-size-70 md-xsmall-size-100 der"
          >
              <h4>
                303 693 3089, 303 693 0422
              </h4>
            <p>
              15433A E. Hampden Av. Aurora, Co, 80013
            </p>
          </div>
        </div>
      </div>              
    </parallax>
    <div class="main main-raised">
      <div class="section profile-content">
        <div class="container">
          <div class="md-layout">
            <div class="md-layout-item md-size-50 mx-auto">
              <div class="profile">
       <!--          <div class="avatar">
                  <img
                    :src="img"
                    alt="Circle Image"
                    class="img-raised rounded-circle img-fluid"
                  />
                </div> -->
                <div class="name">
                  <h3 class="title">Visos Beauty Salon</h3>
                  
                </div>
              </div>
            </div>
          </div>
          <div class="description text-center">
            <p class="text">
              Welcome! Visos Beauty Salon strives to work in making a better version of you! Here at Visos we believe that your hair tells a story. As an important part of your image, your hair projects your identity, your beliefs and moods. We are committed on helping you discover the best version of you by providing you with the talent and technique from our expert stylists, who keep up with the latest trends and give you individual attention. As a Hispanic oriented business, we welcome clients from all cultures and all ages, creating a diverse atmosphere for which we are very proud off.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Tabs } from "@/components";
export default {
  components: {
    Tabs
  },
  bodyClass: "profile-page",
  data() {
  },
  props: {
    header: {
      type: String,
      default: require("@/assets/img/vue-mk-header.jpg")
    },
    img: {
      type: String,
      default: require("@/assets/img/stylist-grey.jpg")
    }
  },
  computed: {
    headerStyle() {
      return {
        backgroundImage: `url(${this.header})`
      };
    }
  }
};
</script>

<style lang="scss" scoped>
@media all and (max-width: 605px) {
h4 {
  font-size: 1.1rem;
}
}
.der {
  text-align: right;
  margin-left: 200px;
}
.profile {
  margin-top: 100px;
}
.description {
  color: #5d5d5d;
}
.section {
  padding: 0;
}
.text {
  margin-bottom: 50px;
}
.profile-tabs /deep/ {
  .md-card-tabs .md-list {
    justify-content: center;
  }

  [class*="tab-pane-"] {
    margin-top: 3.213rem;
    padding-bottom: 50px;

    img {
      margin-bottom: 2.142rem;
    }
  }
}
</style>
