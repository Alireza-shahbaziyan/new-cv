<template>
  <div
    class="
      w-full
      h-screen
      flex flex-col
      lg:flex-row
      justify-center
      items-center
      bg-success
      "
    
  >
    <div
      data-aos="fade-down-right"
      class="flex flex-col lg:w-2/5 justify-center items-center"
    >
      <img
        class="w-2/3 rounded-full md:w-2/4 lg:w-80"
        src="./images/alireza.jpg"
        alt=""
      />
    </div>
    <div class="flex flex-col justify-center items-center">
      <div class="text-white text-2xl md:text-3xl">I'm</div>
      <div
        data-aos="fade-right"
        
        class="
          text-success
          md:text-5xl
          my-4
          text-4xl
          strokeme
          text-center
          uppercase
        "
      >
        {{ event.name }}
      </div>
      <div class="text-white m-4 md:text-4xl text-3xl capitalize">
        <v-typical
          class="blink"
          :steps="['web engineer', 1000, event.jobTitle, 500]"
          :loop="1"
          :wrapper="'h2'"
        >
      </v-typical>
        <!-- BTN -->
      </div>
      <div>
        <button
          class="
            btn btn-outline
            rounded-full
            border-2
            hover:bg-white hover:text-black
            text-white
            md:btn-lg
          "
        >
          Download CV
        </button>
      </div>
    </div>
  </div>
</template>
<script>
import VTypical from "vue-typical";

export default {
  name: "Header",
  props: {
    event: Object,
  },
  components: {
    VTypical,
  },
};
</script>
<style scoped>
.strokeme {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  text-shadow: 0 0 4px white, 0 0 4px white, 0 0 4px white, 0 0 4px white,
    0 0 4px white, 0 0 4px white, 0 0 4px white, 0 0 4px white, 0 0 4px white,
    0 0 4px white, 0 0 4px white, 0 0 4px white, 0 0 4px white, 0 0 4px white,
    0 0 4px white, 0 0 4px white, 0 0 4px white, 0 0 4px white, 0 0 4px white,
    0 0 4px white;
}
</style>