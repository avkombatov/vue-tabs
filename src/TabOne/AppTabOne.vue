<template class="center">
  <div class="container center">
    <div class="tab">
      <app-tab-button
        :color="active === 'one' ? 'active' : ''"
        @action="active = 'one'"
        >One</app-tab-button
      >
      <app-tab-button
        :color="active === 'two' ? 'active' : ''"
        @action="active = 'two'"
        >Two</app-tab-button
      >
        <app-tab-button
        :color="active === 'three' ? 'active' : ''"
        @action="active = 'three'"
        >Three</app-tab-button
      >
        <app-tab-button
        :color="active === 'four' ? 'active' : ''"
        @action="active = 'four'"
        >Four</app-tab-button
      >
        <app-tab-button
        :color="active === 'five' ? 'active' : ''"
        @action="active = 'five'"
        >Five</app-tab-button
      >
      <hr />

      <component :is="componentName"></component>
    </div>
  </div>
</template>

<script>
import AppTabButton from './AppTabButton.vue'
import AppTextOne from './AppTextOne.vue'
import AppTextTwo from './AppTextTwo.vue'
import AppTextThree from './AppTextThree.vue'
import AppTextFour from './AppTextFour.vue'
import AppTextFive from './AppTextFive.vue'
export default {
  data () {
    return {
      active: 'one' // two
    }
  },
  computed: {
    componentName () {
      return 'app-text-' + this.active
    }
  },
  components: { AppTabButton, AppTextOne, AppTextTwo, AppTextThree, AppTextFour, AppTextFive }
}
</script>

<style lang="scss" scoped>
</style>
