<template>
  <div class="w-full flex flex-col items-center relative">
    <HeaderBox :PartName="'About'" :color="`${event.header.color}`"/>
    <div class="lg:w-full lg:flex lg:justify-around items-center">
        <div class="mt-8 flex flex-col items-center justify-center lg:flex-row  lg:h-screen">
      <div class="w-4/5 md:w-3/5 lg:w-1/3 lg:ml-20">
        <img
          class="rounded-xl"
          src="./images/image-about.jpg"
          alt="image-about"
        />
      </div>
      <div class="text-center ">
        <div>
          <div class="font-bold text-3xl capitalize">
            {{ event.header.jobTitle }}
          </div>
          <div class="text-xl text-slate-500 my-2 ">{{ event.about }}</div>
        </div>
        <div class="flex flex-col text-start">
          <div class="flex flex-col md:flex-row justify-around md:items-center ml-4 h-96 lg:h-60 ">
            <div class="md:h-2/4 md:flex md:flex-col md:justify-between">
                <div
              v-for="item in event.AboutOne"
              :key="item"
              class="text-slate-500 mt-2 text-start text-xl font-serif capitalize"
            >
              <span class="text-slate-800 text-xl mx-4"
                >{{ item.itemName }}:</span
              >{{ item.itemKey }}
            </div>
        </div>
            <div class="md:h-2/4 md:flex md:flex-col md:justify-between">
                <div
              v-for="item in event.AboutTow"
              :key="item"
              class="text-slate-500 mt-2 text-start text-xl font-serif capitalize"
            >
              <span class="text-slate-800 text-xl mx-4"
                >{{ item.itemName }}:</span
              >{{ item.itemKey }}
            </div>
            </div>
            
            
          </div>
          <div></div>
        </div>
      </div>
    </div>
    </div>
  </div>
</template>
<script>
import HeaderBox from './HeaderBox.vue';
export default {
    name: "About",
    props: {
        event: Object,
    },
    components: { HeaderBox }
};
</script>
