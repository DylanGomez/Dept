<template>
    <v-container fluid>
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
        <v-navigation-drawer
            v-model="menuOpen"
            absolute
            color="#000"
            width="100%"
        >
            <v-list class="menu">
                <v-list-item-group
                    v-model="selectedItem"
                    class="menu__item-group"
                    active-class="deep-purple--text text--accent-4 icon-active"
                >
                    <v-list-item>
                        <v-list-item-title class="text-list-item">
                            Home
                        </v-list-item-title>
                    </v-list-item>
                    <v-divider></v-divider>

                    <v-list-item>
                        <v-list-item-title class="text-list-item">
                            Werk
                        </v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title class="text-list-item">
                            Over
                        </v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title class="text-list-item">
                            Diensten
                        </v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title class="text-list-item">
                            Partners
                        </v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title class="text-list-item">
                            Stories
                        </v-list-item-title>
                    </v-list-item>
                    <v-list-item>
                        <v-list-item-title class="text-list-item">
                            Vacatures
                        </v-list-item-title>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </v-container>
</template>

<script>

export default {
    name: 'header-component',

    data: () => ({
        menuOpen: false,
        selectedItem: null,

    }),
}
</script>

<style lang="scss">

.header-text {
    font-size: 400px;
    color: #000;
}

.menu {
    &__item-group {
        display: block;
        v-list-item {
        }
    }
}

.text-list-item {
    color: #fff !important;
    font-size: 110px !important;
}

.theme--light.v-divider {
    border-color: #fff !important;
    width: 100vw !important;
}

.icon-active {
    content: "\e5cc";
}

</style>
