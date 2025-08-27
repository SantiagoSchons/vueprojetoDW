<script setup>
import HeaderComponent from '../components/Header.vue'
import FooterComponent from '../components/Footer.vue'
</script>

<template>
  <HeaderComponent />
    
    <FooterComponent />
</template>

<style scoped>
section.projects{
    & ul li{
        & h3{
            font-weight: bold;
            font-size: 1.2rem;
            margin: 0.5rem;
        }
        & p{
            color: #757575;
            font-size: 0.9rem;
            line-height: 1.3rem;
            margin: 0.5rem;
        }

    }
}
</style>
