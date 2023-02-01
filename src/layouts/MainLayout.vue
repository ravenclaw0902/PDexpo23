<template>
  <q-layout view="lHh Lpr lFf">
    <!-- App header -->
    <q-header glossy class="bg-red" elevated>
      <q-toolbar color="white">
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        >
          <q-tooltip class="bg-white text-red">Навигация</q-tooltip>
        </q-btn>
        <q-btn
          flat
          dense
          round
          icon="search"
          aria-label="Search"
          @click="toggleSearch"
        >
          <q-tooltip class="bg-white text-red">Поиск</q-tooltip>
        </q-btn>
        <q-btn
          flat
          dense
          round
          icon="my_location"
          aria-label="NavHelper"
          @click="toggleNavHelper"
        >
          <q-tooltip class="bg-white text-red">Управление</q-tooltip>
        </q-btn>
        <q-item> </q-item>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header>Быстрый доступ</q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>
    <!-- Main section -->
    <q-page-container>
      <router-view />
    </q-page-container>
    <!-- App footer -->
    <q-footer class="bg-red" elevated>
      <q-item></q-item>
    </q-footer>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";

const linksList = [
  {
    title: "Каталог",
    caption: "Продукция компании. Ассортимент и торговые марки",
    type: "section",
    icon: "list",
    link: "../catalog/",
  },
  {
    title: "О компании",
    caption: "Цели и задачи, история и планы на будущее",
    type: "section",
    icon: "badge",
    link: "../about/",
  },
  {
    title: "Контакты",
    caption: "Адреса и телефоны, группы в соцсетях",
    type: "section",
    icon: "chat",
    link: "../contacts/",
  },
];

export default defineComponent({
  name: "MainLayout",

  components: {
    EssentialLink,
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
