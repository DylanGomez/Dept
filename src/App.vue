<template>
    <v-app>
        <header-component> </header-component>
        <v-main>
            <router-view />
        </v-main>
    </v-app>
    </header-component>
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
  font-family: "Teko";
  src: local("Teko"),
   url(./fonts/Teko/Teko-Regular.ttf) format("truetype");
}
@font-face {
  font-family: "Teko SemiBold";
  src: local("Teko Bold"),
   url(./fonts/Teko/Teko-SemiBold.ttf) format("truetype");
}
</style>
