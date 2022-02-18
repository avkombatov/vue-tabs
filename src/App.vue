<template>
<div class="container center">
 <!-- <app-tab-one></app-tab-one> -->
 <app-tab-one-test></app-tab-one-test>

 <app-tab></app-tab>
</div>
</template>

<script>
import AppTabOne from './TabOne/AppTabOne.vue'
import AppTabOneTest from './TabOne/AppTabOneTest.vue'


import AppTab from './TabTest/AppTab.vue'
export default {
  components: {
    AppTabOne, AppTabOneTest,AppTab
  }
}
</script>

<style>

</style>
