<template>
  <div class="breadcrumbs-row">
    <q-breadcrumbs class="text-pink" active-color="red">
      <template v-slot:separator>
        <q-icon size="1.2em" name="arrow_forward" color="red" />
      </template>
      <q-breadcrumbs-el icon="home" to="/" />
      <BreadCrumbs></BreadCrumbs>
    </q-breadcrumbs>
  </div>
  <q-page class="flex flex-center">
    <!--|  Navigation tabs  |-->
    <q-card
      class="custom-tabsname cursor-pointer bg-white relative-position row flex-center"
    >
      <q-tabs align="left">
        <q-route-tab to="../catalog/" label="Каталог" />
        <q-route-tab active to="../contacts/" label="Контакты" />
        <q-route-tab to="../about/" label="О компании" />
      </q-tabs>
    </q-card>

    <!--|  Navigation joystick  |-->
    <q-card
      v-touch-swipe.mouse.up.left.down.right="handleSwipe"
      class="custom-area cursor-pointer bg-white relative-position row flex-center"
    >
      <div class="custom-block"></div>
      <q-btn
        class="glossy custom-button"
        rounded
        push
        no-caps
        size="md"
        color="red"
        to="../"
        label="Назад"
      />
      <div class="custom-block"></div>
      <q-btn
        class="glossy custom-button"
        rounded
        push
        no-caps
        size="md"
        color="red"
        to="../catalog/"
        label="Каталог"
      />
      <div class="custom-block center-block flex flex-center">
        <JoystickButton></JoystickButton>
      </div>
      <q-btn
        class="glossy custom-button"
        rounded
        push
        no-caps
        size="md"
        color="red"
        to="../about/"
        label="О компании"
      />
      <div class="custom-block"></div>
      <div class="custom-block"></div>
      <div class="custom-block"></div>
    </q-card>
  </q-page>
</template>

<style lang="sass" scoped>
.custom-tabsname
  width: 100%
  max-width: 95vw
  height: auto
  max-height: 5vh
  margin: 0 auto auto
  padding: .1%
  border-radius: 0
  box-shadow: none
.custom-area
  width: auto
  max-width: 95vw
  height: auto
  max-height: 75vh
  margin: auto auto .5rem
  padding: .1%
  border-radius: 0
  box-shadow: none
.custom-block
  width: 100%
  max-width: calc(100% / 3)
  height: auto
  min-height: 6rem
  background: none
  color: none
.custom-button
  width: 100%
  max-width: calc(100% / 3)
</style>

<script>
import { defineComponent } from "vue";
import BreadCrumbs from "components/BreadCrumbs.vue";
import JoystickButton from "components/JoystickButton.vue";

export default defineComponent({
  name: "ContactsPage",
  components: {
    BreadCrumbs,
    JoystickButton,
  },
});
</script>
