<template>
  <div class="md:w-1/3 w-11/12  md:m-4">
    <div class="card w-full bg-slate-50 my-4 shadow-xl">
      <figure class="px-10 pt-10">
        <img :src="image" alt="Shoes" class="rounded-xl h-60 w-full" />
      </figure>
      <div class="card-body items-center text-center">
        <h2 class="card-title">{{ cardTitle }}</h2>
        <p>{{ cardText }}</p>
        <div class="card-actions">
          <button :class="`btn btn-${color}`">Show more</button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "QualityItem",
  props: {
    color: String,
    image: String,
    cardTitle: String,
    cardText: String,
  },
};
</script>