<template>
  <div class="tab tab-2">
    <app-button
      v-for="(button, idx) in buttons"
      :button="button"
      :index="idx"
      :key="button"
      :colorBlock="button.openText ? 'tab-2__block-active' : ''"
      :color="button.openText ? 'tab-2__p-active' : ''"
      :colorButton="button.openText ? 'tab-2__block-active' : ''"
      :displayPlus="button.openText ? 'plus__active' : ''"
      :displayMinus="button.openText ? 'minus__active' : ''"
      :descrShow="button.openText ? 'tab-2__descr-active' : ''"
      @open="open"
      >{{ button.title }}</app-button
    >
  
  </div>
</template>

<script>
import AppButton from "./AppButton.vue";

export default {
  data() {
    return {
      buttons: [
        {
          id: 1,
          title: "Как купить страховку на авто?",
          text: "Если Вы хотите самую дешевую страховку, тогда лучше застраховать машину онлайн осаго с нулевой франшизой, можно самую дешевую. Но чтоб была действующей и вела отчисления в МТСБУ. Иначе нужно платить самому при ДТП.",
          openText: false,
        },
        {
          id: 1,
          title: "Как купить страховку на авто?",
          text: "Если Вы хотите самую дешевую страховку, тогда лучше застраховать машину онлайн осаго с нулевой франшизой, можно самую дешевую. Но чтоб была действующей и вела отчисления в МТСБУ. Иначе нужно платить самому при ДТП.",
          openText: false,
        },
        {
          id: 3,
          title: "От какой компании купить ОСАГО?",
          text: "Если Вы хотите самую дешевую страховку, тогда лучше застраховать машину онлайн осаго с нулевой франшизой, можно самую дешевую. Но чтоб была действующей и вела отчисления в МТСБУ. Иначе нужно платить самому при ДТП.",
          openText: false,
        },
        {
          id: 4,
          title: "Страховка ОСАГО или КАСКО?",
          text: "Если Вы хотите самую дешевую страховку, тогда лучше застраховать машину онлайн осаго с нулевой франшизой, можно самую дешевую. Но чтоб была действующей и вела отчисления в МТСБУ. Иначе нужно платить самому при ДТП.",
          openText: false,
        },
        {
          id: 5,
          title: "Где не стоит покупать полис ОСАГО?",
          text: "Если Вы хотите самую дешевую страховку, тогда лучше застраховать машину онлайн осаго с нулевой франшизой, можно самую дешевую. Но чтоб была действующей и вела отчисления в МТСБУ. Иначе нужно платить самому при ДТП.",
          openText: false,
        },
        {
          id: 6,
          title: "Как работает сервис?",
          text: "Если Вы хотите самую дешевую страховку, тогда лучше застраховать машину онлайн осаго с нулевой франшизой, можно самую дешевую. Но чтоб была действующей и вела отчисления в МТСБУ. Иначе нужно платить самому при ДТП.",
          openText: false,
        },
      ],
     
    };
  },
  methods: {
    open(index) {
      this.buttonsLeft = this.buttons.map((button, i) => {
        if (index === i) {
          button.openText = !button.openText;
        } else {
          button.openText = false;
        }
        return button;
      });
    },
     },
  components: {
    AppButton
  },
};
</script>

<style lang="scss" scoped>
</style>