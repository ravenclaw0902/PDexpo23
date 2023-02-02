<template>
  <!--|  BreadCrumbs  |-->
  <div class="flex flex-start breadcrumbs-row"></div>
  <!--|  Main  |-->
  <q-page class="flex flex-center content-section">
    <!--|  Navigation tabs  |-->
    <q-card class="custom-tabsname bg-white relative-position row flex-center">
      <q-tabs>
        <q-route-tab to="../catalog/" label="Каталог" />
        <q-route-tab to="../contacts/" label="Контакты" />
        <q-route-tab to="../about/" label="О компании" />
      </q-tabs>
    </q-card>

    <!--|  Greetings section  |-->
    <q-card class="home-area bg-white relative-position row flex-center">
      <h1></h1>
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
.custom-tabsname
  width: 100%
  max-width: 100%
  height: auto
  max-height: 5vh
  margin: 0 auto auto
  padding: .1%
  border-radius: 0
  box-shadow: none
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
