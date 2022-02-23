<template>
  <div class="tab-4">
    <p class="tab-4__button" @click="$emit('action', index)" :class="back">
      {{ button.title }}
    </p>
  </div>
</template>

<script>
export default {
  props: ["button", "index", "back"],
};
</script>

<style lang="scss" scoped>
</style>