<template>
  <div class="w-full flex flex-col items-center relative">
    <HeaderBox :PartName="'Skills'" :color="event.header.color" />
    <div class="flex flex-col w-full h-96 lg:mt-0 mt-10 justify-around items-center">
      <div data-aos="zoom-in-down" class="flex flex-col lg:flex-row lg:flex-wrap h-1/2 justify-around">
        <div  v-for="i in event.Skills" :key="i.id" class="w-full lg:w-1/2 lg:text-center font-bold">
            {{i.skillName}} <br>
            <progress
            class="progress progress-success w-80 lg:w-96 lg:h-9 h-6 my-1"
            
            :value="i.value"
            max="100"
            ></progress>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderBox from "./HeaderBox.vue";
export default {
  name: "SkillsView",
  components: { HeaderBox },
  props: {
    event: Object,
  },
};
</script>