<template>
  <div class="wrapper">
    <parallax class="section page-header header-filter" :style="headerStyle">
      <div class="container der">
        <div class="md-layout">
          <div class="md-layout-item md-size-50 md-small-size-70 md-xsmall-size-100">
            <h1 class="title">Our Stylists</h1>
              <div class="md-layout-item"></div>
              <div class="md-layout-item"></div>
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
      <div class="section text-center">
        <div class="container">
          <h2 class="title">Here is our team</h2>
          <div class="team">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="img"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      Bertha
                      <br />
                      <small class="card-description text-muted">Stylist</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        We all cut all kinds of hair 
                      </p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        src=@/assets/img/stylist-diana.jpeg
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      Diana
                      <br />
                      <small class="card-description text-muted"
                        >Color Expert</small
                      >
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        We all cut all kinds of hair
                      </p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        src=@/assets/img/stylist-doris.jpeg
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      Doris
                      <br />
                      <small class="card-description text-muted">Color Expert</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        We all cut all kinds of hair 
                      </p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
            </div>
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        src=@/assets/img/stylist-mary.jpeg
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      Mary
                      <br />
                      <small class="card-description text-muted">Stylist</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        We all cut all kinds of hair
                      </p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="img"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      Bertha Bravo
                      <br />
                      <small class="card-description text-muted"
                        >Stylist</small
                      >
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        We all cut all kinds of hair
                      </p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <div class="team-player">
                  <md-card class="md-card-plain">
                    <div class="md-layout-item md-size-50 mx-auto">
                      <img
                        :src="img"
                        alt="Thumbnail Image"
                        class="img-raised rounded-circle img-fluid"
                      />
                    </div>
                    <h4 class="card-title">
                      Bertha Bravo
                      <br />
                      <small class="card-description text-muted">Stylist</small>
                    </h4>

                    <md-card-content>
                      <p class="card-description">
                        We all cut all kinds of hair 
                      </p>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  bodyClass: "landing-page",
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
  data() {
    return {
      name: null,
      email: null,
      message: null
    };
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
@media all and (min-width: 991px) {
.der {
  margin-left: 250px;
}
}
.der {
  text-align: right;
}
.md-card-actions.text-center {
  display: flex;
  justify-content: center !important;
}
.contact-form {
  margin-top: 30px;
}

.md-has-textarea + .md-layout {
  margin-top: 15px;
}
</style>
