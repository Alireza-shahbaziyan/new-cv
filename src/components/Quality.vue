<template>
  <div class="w-full flex flex-col items-center relative">
    <HeaderBox :PartName="'Quality'" :color="event.header.color"/>
  </div>
</template>
<script>
import HeaderBox from "./HeaderBox.vue";
export default {
  name: "quality",
  components: {
    HeaderBox,
  },
  props:{
    event:Object
  }
};
</script>