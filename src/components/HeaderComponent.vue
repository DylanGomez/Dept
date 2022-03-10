<template>
    <v-container fluid>
        <v-parallax
            src="../assets/Images/Header.jpg"
            class="pa-5 parralax"
            height="800"
        >
            <v-app-bar
                absolute
                elevate-on-scroll
                class="app-bar"
            >
                <div class="d-flex align-center">
                    <v-img
                        alt="DEPT Logo"
                        class="shrink mr-2"
                        contain
                        src="../assets/Dept-logo.png"
                        transition="scale-transition"
                        width="60px"
                    />
                </div>

                <v-spacer></v-spacer>

                <v-btn
                    text
                    @click="menuOpen = true"
                >
                    <span class="mr-2">Menu</span>
                    <v-icon>mdi-menu</v-icon>
                </v-btn>
            </v-app-bar>

            <v-row
                align="center"
                justify="center"
                class=""
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
                    class=" case-button"
                >
                    <v-btn dark x-large>
                        View case
                    </v-btn>
                </v-col>
            </v-row>
        </v-parallax>
        <menu-items :opened="menuOpen"></menu-items>
    </v-container>
</template>

<script>

import MenuItems from './Menu.vue'

export default {
    name: 'header-component',

    components: {
        MenuItems,
    },

    data: () => ({
        menuOpen: false,

    }),
}
</script>

<style lang="scss">

.header-text {
    font-size: 400px;
    color: #000;
}

.case-button {
    margin-left: auto !important;
    margin: 1.25rem;
}

.app-bar {
    background-color: transparent !important;
    margin: 0 1.25rem;
}

//mobile scss

@media only screen and (max-width: 768px) {

    .app-bar {
        background-color: #fff !important;
        width: 100%;
        margin: 0;
    }

    .header-text {
        // i removed the header text since I didn't like how it looked, so I drifted a bit from the design
        display: none;
    }

    .parralax {
        height: 250px !important;
        object-fit: cover;
    }
}

</style>
