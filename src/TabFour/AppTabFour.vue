<template>
  <div class="tab tab-4">
    <div class="tab-4__buttons">
      <app-button
        v-for="(button, idx) in buttons"
        :key="button"
        :index="idx"
        :button="button"
        :back="active === idx ? 'tab-4__button-active' : ''"
        @action="active = idx"
      ></app-button>
    </div>
    <component :is="componentName"></component>
    <!-- <app-text-1></app-text-1> -->
  </div>
</template>

<script>
import AppButton from './AppButton.vue'
import AppText1 from './AppText1.vue'
import AppText2 from './AppText2.vue'
import AppText3 from './AppText3.vue'

export default {
  data () {
    return {
      active: 0,
      buttons: [
        {
          id: 1,
          title: 'Tab-1'
        },
        {
          id: 2,
          title: 'Tab-2'
        },
        {
          id: 3,
          title: 'Tab-3'
        }
      ]
    }
  },
  computed: {
    componentName () {
      return 'app-text-' + (this.active + 1)
    }
  },
  components: {
    AppButton,
    AppText1,
    AppText2,
    AppText3
  }
}
</script>

<style lang="scss" scoped>
</style>
