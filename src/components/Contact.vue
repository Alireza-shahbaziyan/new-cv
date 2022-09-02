<template>
  <div class="w-full h-screen flex flex-col items-center relative">
    <HeaderBox :PartName="'Contact me'" />
</div>
<div>alireza</div>
</template>
<script>
import HeaderBox from "./HeaderBox.vue";
export default {
  name: "Contact",
  components: {
    HeaderBox,
  },
  props: {
    Color: Object,
  },
};
</script>