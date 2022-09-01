<template>
  <div class=" sticky top-0 z-50 h-24">
    <div class="relative ">
    <div class="navbar  absolute bg-slate-50 flex flex-col justify-start items-start">
    <div class="w-full">
      <div class="flex-1">
        <button class="btn btn-ghost text-2xl font-serif">{{ logo.logo }}</button>
      </div>
      <div class="flex-none">
        <label  class="btn btn-success swap swap-rotate">
          <!-- this hidden checkbox controls the state -->
          <input @click="showMenu = !showMenu" type="checkbox" />

          <!-- hamburger icon -->
          <svg
            class="swap-off fill-current"
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 512 512"
          >
            <path
              d="M64,384H448V341.33H64Zm0-106.67H448V234.67H64ZM64,128v42.67H448V128Z"
            />
          </svg>

          <!-- close icon -->
          <svg
            class="swap-on fill-current"
            xmlns="http://www.w3.org/2000/svg"
            width="32"
            height="32"
            viewBox="0 0 512 512"
          >
            <polygon
              points="400 145.49 366.51 112 256 222.51 145.49 112 112 145.49 222.51 256 112 366.51 145.49 400 256 289.49 366.51 400 400 366.51 289.49 256 400 145.49"
            />
          </svg>
        </label>
      </div>
    </div>
    <div v-show="showMenu">
      <ul
        class="flex flex-col justify-start items-start menu menu-horizontal p-0"
      >
        <li><a class="capitalize font-sans">about</a></li>
        <li><a class="capitalize font-sans">Quality</a></li>
        <li><a class="capitalize font-sans">Skills</a></li>
        <li><a class="capitalize font-sans">contact</a></li>
      </ul>
    </div>
  </div>
  </div>
  </div>
</template>
<script>
export default {
  name: "Navabar",
  props: {
    logo: Object,
  },
  data() {
    return {
        showMenu:false
    }
  },
};
</script>