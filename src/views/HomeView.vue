<script>
import Header from "../components/Header.vue";
import About from "../components/About.vue";
import Navbar from "./Navbar.vue";
import Quality from "../components/Quality.vue";
import SkillsView from "../components/SkillsView.vue";

import Contact from "../components/Contact.vue";
import Footer from "../components/Footer.vue";
export default {
  components: {
    Header,
    About,
    Navbar,
    Quality,
    SkillsView,
    Contact,
    Footer
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
        Quality:[
        {id:1,image:'https://cdn.dribbble.com/users/808342/screenshots/14930079/media/56de2ce055bbdbf7ec8a0515c6489448.jpg?compress=1&resize=400x400',cardTitle:"A page",cardText:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, eum."},
        {id:2,image:'https://themewagon.com/wp-content/uploads/2020/10/Anime.png',cardTitle:"Anime page",cardText:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, eum."},
        {id:3,image:'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQQz-Z7fqJZlH7xMl61fILtCUY0mgexj8pCzA&usqp=CAU',cardTitle:"Amozegar",cardText:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloribus, eum."}
      ],
      Skills:[
        {id:1,skillName:"javaScript",value:"93",color:"warning"},
        {id:2,skillName:"HTML",value:"92",color:"error"},
        {id:3,skillName:"CSS",value:"92",color:"info"},
        {id:4,skillName:"Bootstrap",value:"85",color:"secondary"},
        {id:5,skillName:"tailwindcss",value:"87",color:"primary"},
        {id:6,skillName:"Vue-js",value:"90",color:"success"},
      ]
      },
      
    };
  },
};
</script>


<template>
  <Header :event="events.header"/>
  <Navbar :logo="events.header"/>
  <About :event="events"  class="my-12"/>
  <Quality :event="events" class="my-12"/>
  <SkillsView :event="events" class="my-12"/>
  <Contact class="my-12"/>
  <Footer/>
  
</template>
