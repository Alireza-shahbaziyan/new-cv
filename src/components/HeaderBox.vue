<template>
<div
      class="
        text-white text-5xl
        md:text-9xl
        strokeme
        uppercase
        opacity-10
        font-sans font-extrabold
      "
    >
      {{PartName}}
    </div>
    <div class="text-success font-bold font-sans text-4xl absolute top-10">
        {{PartName}}
    </div>
</template>
<script>
    export default{
        name:"HeaderBox",
        props:{
            PartName:String,
            color:String
        }
    }
</script>
<style scoped>
    .strokeme {
      color: white;
      text-shadow: -1px -1px 0 #000, 1px -1px 0 #000, -1px 1px 0 #000,
        1px 1px 0 #000;
    }
    </style>