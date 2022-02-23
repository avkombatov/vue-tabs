<template>
  <div class="container center">
    <!-- <app-tab-one></app-tab-one> -->
    <app-tab-one-test></app-tab-one-test>
    <app-tab></app-tab>
    <app-tab-three></app-tab-three>
    <app-tab-four></app-tab-four>
  </div>
</template>

<script>
import AppTabOne from './TabOne/AppTabOne.vue'
import AppTabOneTest from './TabOne/AppTabOneTest.vue'
import AppTab from './TabTwo/AppTab.vue'
import AppTabThree from './TabThree/AppTabThree.vue'
import AppTabFour from './TabFour/AppTabFour.vue'
export default {
  components: {
    AppTabOne,
    AppTabOneTest,
    AppTab,
    AppTabThree,
    AppTabFour
  }
}
</script>

<style>
</style>
