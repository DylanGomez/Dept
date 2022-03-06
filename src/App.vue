<template>
    <v-app>
        <header-component> </header-component>
        <v-main>
            <router-view />
        </v-main>
    </v-app>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'

export default {
    name: 'app',

    components: {
        HeaderComponent,
    },

    data: () => ({
    }),
}
</script>

<style lang="scss">
@import 'src/scss/variables.scss';

.v-application {
   font-family: $body-font-family !important;
   margin: 1.5rem 2rem;
   width: 100vw;
}

@font-face {
  font-family: "Teko Bold";
  src: local("Teko Bold"),
   url(./fonts/Teko/Teko-Bold.ttf) format("truetype");
}
@font-face {
  font-family: "Teko Light";
  src: local("Teko Light"),
   url(./fonts/Teko/Teko-Light.ttf) format("truetype");
}
@font-face {
  font-family: "Teko Medium";
  src: local("Teko Medium"),
   url(./fonts/Teko/Teko-Medium.ttf) format("truetype");
}
@font-face {
  font-family: "Teko Regular";
  src: local("Teko Regular"),
   url(./fonts/Teko/Teko-Regular.ttf) format("truetype");
}
@font-face {
  font-family: "Teko SemiBold";
  src: local("Teko Bold"),
   url(./fonts/Teko/Teko-SemiBold.ttf) format("truetype");
}
</style>
