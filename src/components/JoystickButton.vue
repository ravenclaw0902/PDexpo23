<template>
  <!-- NavHelper -->
  <svg
    class="joystick"
    width="380"
    height="380"
    viewBox="0 0 380 380"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      class="animate-faster joy-elem joy-top"
      d="M190 0L235.073 87.5693C221.453 80.9512 206.16 77.2393 190 77.2393C173.84 77.2393 158.547 80.9512 144.927 87.5693L190 0Z"
      fill="inherit"
    />
    <path
      class="animate-faster joy-elem joy-right"
      d="M302.761 190C302.761 206.159 299.049 221.452 292.431 235.072L380 190L292.431 144.928C299.049 158.548 302.761 173.841 302.761 190Z"
      fill="inherit"
    />
    <path
      class="animate-faster joy-elem joy-bottom"
      d="M144.927 292.431C158.547 299.049 173.84 302.761 190 302.761C206.16 302.761 221.453 299.049 235.073 292.431L190 380L144.927 292.431Z"
      fill="inherit"
    />
    <path
      class="animate-faster joy-elem joy-left"
      d="M72.4893 190C72.4893 173.841 76.2012 158.548 82.8193 144.928L0 190L82.8193 235.072C76.2012 221.452 72.4893 206.159 72.4893 190Z"
      fill="inherit"
    />
    <path
      class="animate-faster joy-elem joy-center"
      d="M190 285C242.467 285 285 242.467 285 190C285 137.533 242.467 95 190 95C137.533 95 95 137.533 95 190C95 242.467 137.533 285 190 285Z"
      fill="inherit"
    />
  </svg>
</template>
<style lang="sass" scoped>
.joystick
  width: 100%
  max-width: 6rem
  height: auto
  margin: auto
.joy-elem
  fill: #f44336
.joy-elem:hover
  opacity: .75
</style>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "JoystickButton",
  props: {
    tip: {
      type: String,
      required: true,
    },

    caption: {
      type: String,
      default: "",
    },

    link: {
      type: String,
      default: "#",
    },

    status: {
      type: String,
      default: "visible",
    },
  },
});
</script>
