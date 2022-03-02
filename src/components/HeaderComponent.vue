<template>
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
</template>

<script>

export default {
    name: 'header-component',

    components: {

    },
}
</script>
