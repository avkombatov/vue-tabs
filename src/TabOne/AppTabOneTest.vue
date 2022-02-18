<template class="center">
  <div class="tab">
    <app-tab-button
      v-for="(button, idx) in buttons"
      :key="button"
      :color="active === idx ? 'active' : ''"
      @action="active = idx"
      >{{ button }}
    </app-tab-button>
    <hr />
    <component :is="componentName"></component>
  </div>
</template>

<script>
import AppTabButton from "./AppTabButton.vue";
import AppTextOne from "./AppTextOne.vue";
import AppTextTwo from "./AppTextTwo.vue";
import AppTextThree from "./AppTextThree.vue";
import AppTextFour from "./AppTextFour.vue";
import AppTextFive from "./AppTextFive.vue";
export default {
  data() {
    return {
      buttons: ["one", "two", "three", "four", "five"],
      active: 0,
      button: "",
    };
  },
  computed: {
    componentName() {
      return "app-text-" + this.buttons[this.active];
    },
  },
  components: {
    AppTabButton,
    AppTextOne,
    AppTextTwo,
    AppTextThree,
    AppTextFour,
    AppTextFive,
  },
};
</script>

<style lang="scss" scoped>
</style>
