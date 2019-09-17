<template>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <nav>
        <ul>
          <li>
            <router-link to="/stylists">
              <p class="md-list-item-content">Stylists</p>
            </router-link> 
          </li>
          <li>
            <router-link to="/contact">
              <p class="md-list-item-content">Contact</p>
            </router-link> 
          </li>
          <li class="redesfooter">
            <md-list-item
              href="https://www.facebook.com/CreativeTim"
              target="_blank"
            >
              <i class="fab fa-facebook-square"></i>
              <p class="hidden-lg">Facebook</p>
              <md-tooltip md-direction="bottom">Like us on Facebook</md-tooltip>
              </md-list-item>
          </li>
          <li class="redesfooter">
              <md-list-item
                href="https://www.instagram.com/CreativeTimOfficial"
                target="_blank"
              >
                <i class="fab fa-instagram"></i>
                <p class="hidden-lg">Instagram</p>
                <md-tooltip md-direction="bottom"
                  >Follow us on Instagram</md-tooltip
                >
              </md-list-item>
          </li>
        </ul>
      </nav>
      <div class="copyright">
        &copy; {{ year }}, Visos Beauty Salon 
        15433A E. Hampden Av. Aurora, Co, 80013 
      </div>
      <div class="copyright">
        <strong>
          303 693 3089 - 303 693 0422 
        </strong>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String
  },
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
};
</script>
<style scoped>
a.md-list-item {
  margin-top: 10px;
}
</style>
