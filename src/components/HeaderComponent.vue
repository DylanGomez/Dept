<template>
    <v-parallax
        src="../assets/Images/Header.jpg"
        height="800"
        class="pa-5"
    >
        <v-app-bar
            app
            color="transparent"
            absolute
            elevate-on-scroll
            class="mx-5"
        >
            <div class="d-flex align-center">
                <v-img
                    alt="DEPT Logo"
                    class="shrink mr-2"
                    contain
                    src="../assets/Dept-logo.png"
                    transition="scale-transition"
                    width="60"
                />
            </div>

            <v-spacer></v-spacer>

            <v-btn
                href="https://github.com/vuetifyjs/vuetify/releases/latest"
                target="_blank"
                text
            >
                <span class="mr-2">Menu</span>
                <v-icon>mdi-menu</v-icon>
            </v-btn>
        </v-app-bar>

        <v-row
            align="center"
            justify="center"
        >
            <v-col>
                <h1 class="header-text ml-3">
                    Work
                </h1>
            </v-col>
        </v-row>

        <v-row align="end">
            <v-col
                cols="auto"
                class="ml-auto ma-5"
            >
                <v-btn dark x-large>
                    View case
                </v-btn>
            </v-col>
        </v-row>
    </v-parallax>
</template>

<script>

export default {
    name: 'header-component',

    components: {

    },
}
</script>

<style lang="scss">

.header-text {
    font-size: 400px;
    color: #000;
}

</style>
