<script>
import Header from "../components/Header.vue";
import About from "../components/About.vue";
import Navbar from "./Navbar.vue";
import Quality from "../components/Quality.vue";

export default {
  components: {
    Header,
    About,
    Navbar,
    Quality
},
  data() {
    return {
      events: {
        header: {
          logo: "ARS",
          name: "alireza shahbaziyan",
          jobTitle: "frontend developer",
          color:"success",
        },
        about:
          "Lorem, ipsum dolor sit amet  distinctio, accusamus ex itaque animi sunt quis ipsam perferendis magnam tempora nemo, vero hic",
        AboutOne: [
          { itemName: "Birthday", itemKey: "July 19,2001" },
          { itemName: "Degree", itemKey: "master" },
          { itemName: "Experience", itemKey: "2 years" },
          { itemName: "Phone", itemKey: "+98939262555" },
        ],
        AboutTow: [
          { itemName: "Email", itemKey: "a.alireza-shahbaziyan.ir" },
          { itemName: "Address", itemKey: "123 street,new york" },
          { itemName: "Job_types", itemKey: "Contract" },
          { itemName: "Workplaces", itemKey: "On-site ,Remote" },
        ],
      },
    };
  },
};
</script>


<template>
  <Header :event="events.header" />
  <Navbar :logo="events.header" />
  <About :event="events" />
  <Quality :event="events"/>

</template>
