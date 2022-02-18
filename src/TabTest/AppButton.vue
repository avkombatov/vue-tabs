<template>
  <div class="tab-2__block" :class="colorBlock">
    <div class="tab-2__button" @click="$emit('open', index)" :class="colorButton">
      <div class="tab-2__button-left">
        <div class="tab-2__circle-question">
          <p class="tab-2__quesion">?</p>
        </div>
        <p class="tab-2__p" :class="color"><slot /></p>
      </div>
      <div class="tab-2__circle-plus">
        <span class="plus" :class="displayPlus">+</span><span class="minus" :class="displayMinus">-</span>
      </div>
    </div>
    <p class="tab-2__descr-p" :class="descrShow">
      {{ button.text }}
    </p>
  </div>
</template>

<script>
export default {
  emits: ["open"],
  props: ["button", "index", "color", "openText", "descrShow","colorBlock", "colorButton","displayPlus","displayMinus"],
};
</script>

<style lang="scss" scoped>
</style>