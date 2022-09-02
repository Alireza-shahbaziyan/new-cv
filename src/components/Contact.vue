<template>
  <div class="w-full h-screen flex flex-col items-center relative">
    <HeaderBox :PartName="'Contact me'" />
    <div class="w-10/12 lg:w-full flex flex-col text-center my-14">
      <div class="flex flex-col w-full md:items-center">
        <input type="text" placeholder="Your Name" class="input rounded-3xl mt-4 input-bordered w-full max-w-xs" />
        <input type="email" placeholder="Your Email" class="input rounded-3xl mt-4 input-bordered w-full max-w-xs" />
      </div>
      <div class="">
        <input type="text" placeholder="Subject" class="input input-bordered rounded-3xl mt-4 w-full max-w-xs" />
      </div>
      <div>
        <textarea class="textarea w-full lg:w-2/4 mt-4 textarea-bordered h-44 rounded-3xl" placeholder="Message"></textarea>
      </div>
      <div class="w-full text-center mt-4">
        <button class="btn btn-outline btn-success rounded-full">Send message</button>
      </div>
    </div>
</div>

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