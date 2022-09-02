<template>
  <div class="w-full flex flex-col items-center relative">
    <HeaderBox :PartName="'EXPERICENCE'" :color="event.header.color" />
    <div
      class="
      my-10
        w-full
        flex flex-col
        md:flex-row
        md:flex-wrap
        lg:flex-nowrap  
        justify-center
        items-center
      "
    >
      <QualityItem
      data-aos="zoom-in-up"
      v-for="i in event.Quality"
        :key="i.id"
        :image="i.image"
        :cardText="i.cardText"
        :cardTitle="i.cardTitle"
        :color="event.header.color"
      />
    </div>
  </div>
</template>
<script>
import HeaderBox from "./HeaderBox.vue";
import QualityItem from "./QualityItem.vue";

export default {
  name: "quality",
  components: {
    HeaderBox,
    QualityItem,
  },
  props: {
    event: Object,
  },
};
</script>