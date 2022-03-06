<template>
    <v-card
        class="client-card ma-auto"
        flat
    >
        <v-img
            v-if="imageUrl"
            class="image"
            :src="require(`../assets/Logos/${imageUrl}`)"
            max-width="250px"
        ></v-img>
    </v-card>
</template>

<script>

export default {
    name: 'client-block',

    props: {
        imageUrl: {
            type: String,
            default: null,
        },
    },

}
</script>

<style lang="scss">

.client-card {
    justify-self: center;
    height: 150px;
    align-items: center;
    mix-blend-mode: multiply;
}

</style>
