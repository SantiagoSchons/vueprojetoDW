<script setup>
import HeaderComponent from '../components/Header.vue'
import FooterComponent from '../components/Footer.vue'
import { ref } from 'vue'

const home = ref([
        {
          id: 1,
          title: "ShopEase",
          image: "shopease.png",
          description: null,
          categorias: ['Mobile', 'Application', 'E-commerce'],
          classe: null,
        },
        {
          id: 2,
          title: "Insightly",
          description:"Developed a SaaS-based analytics dashboard for Insightly, focusing on providing actionable insights through a user-centric design. The dashboard improved data accessibility and was adopted by 80% of users within the first three months.",
          image: null,
          classe: 'emogi',
          categorias: ['Web 3.0', 'HTML', 'Dashboard'],
        },

])


</script>

<template>
  <HeaderComponent />
    <main>
        <section class="banner">

            <h1>Hi, I’m <span>Alex</span></h1>

            <p>
                a <strong>UI/UX Designer</strong> based in <strong>Los Angeles</strong>. With over <strong>3 years of experience</strong>, I specialize in creating
                user-friendly digital products that solve real-world problems.
            </p>
        </section>

        <section class="cards">
            <ul>
                <li v-for="carts in home">
                    <h3>{{ carts.title }}</h3>
                    <p v-if="carts.image != null">
                        <img :src="'/images/'+carts.image" alt="Imagem celular">
                    </p>
                    <p v-if="carts.description != null">
                        <p :class="carts.classe">💡</p>
                        {{ carts.description }}
                    </p>
                    <ul>
                        <li v-for="f in carts.categorias">
                            {{ f }}
                        </li>
                    </ul>
                </li>
            </ul>
        </section>
    </main>
    <FooterComponent />
</template>

<style scoped>
section.cards>ul {
    &>li {
        background: white;
        border-radius: 10px;
        padding: 20px;
        margin-bottom: 20px;

        & h3 {
            font-size: 1.5rem;
        }

        & img {
            border-radius: 10px;
        }

        & .emogi {
            font-size: 4rem;
        }
    }

    & ul {
        display: flex;
        margin-top: 20px;

        & li:first-child {
            margin-left: 0;
        }

        & li {
            background: rgb(232, 232, 232);
            color: black;
            margin: 0 10px;
            padding: 4px 8px;
            border-radius: 10px;
            font-size: 0.7rem;
            font-weight: bold;
        }
    }
}
</style>
