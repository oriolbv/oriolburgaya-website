<template>
  <div id="app">
    <desktop-nav id="desktop-nav"/>
    <mobile-nav id="mobile-nav"/>
    <div class="view-container">
      <router-view/>
    </div>
  </div>
</template>

<script>
import DesktopNav from '@/components/DesktopNav'
import MobileNav from '@/components/MobileNav'


export default {
  data: function () {
        return {
            
        }
    },
  components: {
    DesktopNav,
    MobileNav
  }
}
</script>

<style lang="sass" scoped>
.view-container
  width: 79vw
  padding: 1.5em
  margin-left: 20vw
  box-sizing: border-box
  min-height: 100vh
  background-image: url("./assets/images/background.png");
  background-repeat: no-repeat;
  background-size: 100% 100%;
#mobile-nav
  display: none
@media screen and (max-width: 1096px)
  .view-container
    width: 100%
    margin-left: 0
  #desktop-nav
    display: none
  #mobile-nav
    display: flex
</style>