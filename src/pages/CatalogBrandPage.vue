<template>
  <!--|  BreadCrumbs  |-->
  <div class="flex flex-start breadcrumbs-row">
    <q-breadcrumbs class="text-red" active-color="red">
      <template v-slot:separator>
        <q-icon size="1.2em" name="arrow_forward" color="red" />
      </template>
      <q-breadcrumbs-el icon="home" to="/" />
      <BreadCrumbs></BreadCrumbs>
    </q-breadcrumbs>
  </div>
  <!--|  Main  |-->
  <q-page class="flex flex-center content-section">
    <!--|  Navigation tabs  |-->
    <q-card
      class="custom-tabsname cursor-pointer bg-white relative-position row flex-center"
    >
      <q-tabs align="left">
        <q-route-tab active to="../catalog/" label="Каталог" />
        <q-route-tab to="../contacts/" label="Контакты" />
        <q-route-tab to="../about/" label="О компании" />
      </q-tabs>
    </q-card>
    <!--|  Brand page content  |-->
    <q-item class="flex flex-center">
      <BrandCard></BrandCard>
      <BrandItemList></BrandItemList>
    </q-item>
    <!--|  Navigation joystick  |-->
    <q-card
      v-touch-swipe.mouse.up.left.down.right="handleSwipe"
      class="joystick-area cursor-pointer bg-white relative-position row flex-center"
    >
      <div class="joystick-block"></div>
      <q-btn
        class="glossy joystick-button"
        rounded
        push
        no-caps
        size="md"
        color="red"
        to="../"
        label="Назад"
      />
      <div class="joystick-block"></div>
      <div class="joystick-block"></div>
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
  max-width: 95vw
  height: auto
  max-height: 5vh
  margin: 0 auto auto
  padding: .1%
  border-radius: 0
  box-shadow: none
</style>

<script>
import { defineComponent } from "vue";
import BreadCrumbs from "components/BreadCrumbs.vue";
import BrandCard from "components/BrandCard.vue";
import BrandItemList from "components/BrandItemList.vue";
import JoystickButton from "components/JoystickButton.vue";

export default defineComponent({
  name: "CatalogBrandPage",
  components: {
    BreadCrumbs,
    BrandCard,
    BrandItemList,
    JoystickButton,
  },
});
</script>
