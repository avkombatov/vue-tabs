<template>
  <div class="container center">
    <!-- <app-tab-one></app-tab-one> -->
    <app-tab-one-test></app-tab-one-test>
    <app-tab></app-tab>
    <app-tab-three></app-tab-three>
  </div>
</template>

<script>
import AppTabOne from "./TabOne/AppTabOne.vue";
import AppTabOneTest from "./TabOne/AppTabOneTest.vue";
import AppTab from "./TabTwo/AppTab.vue";
import AppTabThree from "./TabThree/AppTabThree.vue";
export default {
  components: {
    AppTabOne,
    AppTabOneTest,
    AppTab,
    AppTabThree,
  },
};
</script>

<style>
</style>
