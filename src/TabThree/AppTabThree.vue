<template>
  <div class="tab tab-3">
    <app-button
      v-for="(button, idx) in buttons"
      :key="button"
      :button="button"
      :index="idx"
      @open="open"
      :colorTitle="button.isOpen ? 'tab-3__title-active' : ''"
      :plusActive="button.isOpen ? 'tab-3__plus-active' : ''"
       :minusActive="button.isOpen ? 'tab-3__minus-active' : ''"
    ></app-button>
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
          title: "Как сделать заказ?",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat hic reiciendis voluptas vel optio recusandae neque soluta sit? Nulla a ducimus alias iusto facilis maxime ratione officiis ipsam sapiente non!",
          isOpen: false,
        },
        {
          id: 2,
          title: "Способы оплаты",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat hic reiciendis voluptas vel optio recusandae neque soluta sit?",
          isOpen: false,
        },
        {
          id: 3,
          title: "Доставка",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias tenetur atque saepe eum obcaecati fuga aliquam incidunt. Aliquam debitis obcaecati officiis quas, similique dolor laboriosam molestiae placeat in saepe aperiam adipisci reprehenderit soluta beatae, quos vitae inventore, rerum amet tempore! Repellendus quos dicta eveniet totam molestiae quibusdam dolore fuga cum velit nobis nihil facilis delectus, excepturi doloribus sed, illo ipsam!",
          isOpen: false,
        },
          {
          id: 4,
          title: "Сроки доставки",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias tenetur atque saepe eum obcaecati fuga aliquam incidunt. Aliquam debitis obcaecati officiis quas, similique dolor laboriosam molestiae placeat in saepe aperiam adipisci reprehenderit soluta beatae, quos vitae inventore, rerum amet tempore!",
          isOpen: false,
        },
          {
          id: 4,
          title: "Как сделать обмен?",
          text: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias tenetur atque saepe eum obcaecati fuga aliquam incidunt. Aliquam debitis obcaecati officiis quas",
          isOpen: false,
        },
          {
          id: 5,
          title: "Как сделать обмен?",
          text: " Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias tenetur atque saepe eum obcaecati fuga aliquam incidunt. Aliquam debitis obcaecati officiis quas, similique dolor laboriosam molestiae placeat in saepe aperiam adipisci reprehenderit soluta beatae, quos vitae inventore, rerum amet tempore! Repellendus quos dicta eveniet totam molestiae quibusdam dolore fuga cum velit nobis nihil facilis delectus, excepturi doloribus sed, illo ipsam!",
          isOpen: false,
        },
           {
          id: 6,
          title: "Куда и когда вернутся деньги за возвращённый товар?",
          text: " Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias tenetur atque saepe eum obcaecati fuga aliquam incidunt. Aliquam debitis obcaecati officiis quas, similique dolor laboriosam molestiae placeat in saepe aperiam adipisci reprehenderit soluta beatae, quos vitae inventore, rerum amet tempore!",
          isOpen: false,
        },
      ],
    };
  },
  methods: {
   
    open(index) {
      this.buttons = this.buttons.map((button, i) => {
        if (index === i) {
          button.isOpen = !button.isOpen;
        }
        return button;
      });
    },
  },
  components: {
    AppButton,
  },
};
</script>

<style lang="scss" scoped>
</style>