<template>
  <div class="tab-3">
    <div class="tab-3__top" @click="$emit('open', index)">
      <p class="tab-3__title" :class="colorTitle">{{ button.title }}</p>
      <span class="tab-3__plus" :class="plusActive">+</span>
      <span class="tab-3__minus" :class="minusActive">-</span>
    </div>
    <hr />
    <p class="tab-3__descr" v-if="button.isOpen">
      {{ button.text }}

    </p>
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  },

  props: ['button', 'colorTitle', 'index', 'plusActive', 'minusActive']

}
</script>

<style lang="scss" scoped>
</style>
