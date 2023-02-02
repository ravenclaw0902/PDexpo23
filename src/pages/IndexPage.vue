<template>
  <!--|  BreadCrumbs  |-->
  <div class="flex flex-start breadcrumbs-row"></div>
  <!--|  Main  |-->
  <q-page class="flex flex-center content-section">
    <!--|  Greetings section  |-->
    <q-card class="home-area bg-white relative-position row flex-center">
      <h1 class="home-title">АО «РУССКИЙ ПРОДУКТ»</h1>
      <h3 class="home-subtitle">
        Лучшие традиции отечественного пищевого производства!
      </h3>
      <div class="flex home-descr">
        <p class="first">
          <span>«РУССКИЙ ПРОДУКТ»</span> – крупный отечественный производитель
          продуктов питания, который стабильно улучшает качество своей продукции
          уже более <span>25</span> лет.
        </p>
        <p class="second">
          <span>«РУССКИЙ ПРОДУКТ»</span> сохраняет лучшие традиции пищевой
          индустрии. Компания бережно относится к преемственности поколений, при
          этом движется в ногу со временем и соответствует международным
          стандартам качества.
        </p>
        <p class="third">
          Продукция компании представлена более чем в
          <span>70 000</span> торговых точек, включая федеральные сети и
          онлайн-торговлю. Сбытовая сеть – <span>140</span>
          контрагентов на территории РФ и за границей.
        </p>
        <p class="forth">
          <span>«РУССКИЙ ПРОДУКТ»</span> экспортирует в Армению, Грузию,
          Беларусь, Казахстан, Кыргызскую Республику, Абхазию, Корею, Кувейт,
          Монголию, Таджикистан, Туркменистан, Узбекистан, Германию, Грецию,
          Израиль, Латвию, Литву, Молдавию, Канаду и активно развивает азиатское
          экспортное направление – Индия и Китай.
        </p>
      </div>
    </q-card>

    <!--|  Navigation joystick  |-->
    <q-card
      v-touch-swipe.mouse.up.left.down.right="handleSwipe"
      class="joystick-area cursor-pointer bg-white relative-position row flex-center"
    >
      <div class="joystick-block"></div>
      <div class="joystick-block"></div>
      <div class="joystick-block"></div>
      <q-btn
        class="glossy joystick-button"
        rounded
        push
        no-caps
        size="md"
        color="red"
        to="../catalog/"
        label="Каталог"
      />
      <div class="joystick-block center-block flex flex-center">
        <JoystickButton></JoystickButton>
      </div>
      <q-btn
        class="glossy joystick-button"
        rounded
        push
        no-caps
        size="md"
        color="red"
        to="../about/"
        label="О компании"
      />
      <div class="joystick-block"></div>
      <q-btn
        class="glossy joystick-button"
        rounded
        push
        no-caps
        size="md"
        color="red"
        to="../contacts/"
        label="Контакты"
      />
      <div class="joystick-block"></div>
    </q-card>
  </q-page>
</template>

<style lang="sass" scoped>
.home-area
  width: calc(100% / 6 * 5)
  margin: auto
  border: none
  box-shadow: none
.home-title
  font-size: 4rem
  margin: 1rem auto
.home-subtitle
  margin: 1rem auto 2.5rem
  font-size: 2.5rem
.home-descr
  width: 90%
  margin: auto
.home-descr p
  padding: .5rem 0
  text-align: justify
.home-descr p.first
  margin: auto 6% auto -6%
.home-descr p.second
  margin: auto 2% auto -2%
.home-descr p.third
  margin: auto -2% auto 2%
.home-descr p.forth
  margin: auto -6% auto 6%
.home-descr p span
  color: var(--elem-red-100)
  font-weight: 600
</style>

<script>
import { defineComponent } from "vue";
import JoystickButton from "components/JoystickButton.vue";

export default defineComponent({
  name: "IndexPage",
  components: {
    JoystickButton,
  },
});
</script>
