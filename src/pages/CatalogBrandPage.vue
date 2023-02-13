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
    <!--|  Brand card  |-->
    <q-card class="brand-area bg-white relative-position row flex-center">
      <BrandCard></BrandCard>
    </q-card>
    <q-card class="brand-area bg-white relative-position row flex-center">
      <BrandItemList></BrandItemList>
    </q-card>
    <!--|  Navigation joystick  |-->
    <q-card
      v-touch-swipe.mouse.up.left.down.right="handleSwipe"
      class="joystick-area cursor-pointer bg-white relative-position row flex-center"
    >
      <div class="joystick-block center-block flex flex-center">
        <JoystickButton></JoystickButton>
      </div>
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
