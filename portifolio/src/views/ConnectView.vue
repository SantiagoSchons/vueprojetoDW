<script setup>
import HeaderComponent from '../components/Header.vue'
import FooterComponent from '../components/Footer.vue'
import { ref } from 'vue'

const connect = ref([
    {
        id: 1,
        title: "Instagram",
        classe: "fa-brands fa-instagram",
        link: "#",
    },
    {
        id: 2,
        title: "Behance",
        classe: "fa-brands fa-behance", 
        link: "#",
    },
    {
        id: 3,
        title: "Dribble",
        classe: "fa-brands fa-dribbble", 
        link: "#",
    },
    {
        id: 4,
        title: "LinkedIn",
        classe: "fa-brands fa-linkedin-in", 
        link: "#",
    },
]);



</script>
 

<template>
  <HeaderComponent />
    <main>
        <section class="banner">

            <h1><span>Connect</span></h1>

            <p>
                I’m always open to new opportunities and collaborations. Whether you’re looking to start a project or just want to chat, feel free to reach out.
            </p>
        </section>

        <section class="connect">
            <ul class="white-itens"> 
                <li v-for="connects in connect">
                    <a :href="connects.link"><span :class="connects.classe"></span>{{ connects.title }}</a>
                </li>
            </ul>
        </section>
    </main>
    <FooterComponent />
</template>

<style scoped>
section.connect {
    & ul {
        & li {
            text-align: center;
            & span {
                font-weight:bold ;
                padding: 0 15px 0 0;
            }
        } 
    }
}
</style>
