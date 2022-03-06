<template>
    <v-card
        class="case-card"
        :style="`gridColumn: ${gridColumn}; gridRow:${gridRow};`"
        flat
    >
        <v-img
            v-if="imageUrl"
            :src="require(`../assets/Images/${imageUrl}`)"
            height="500px"
            width="40rem"
        ></v-img>

        <v-card-title class="case-card__title">
            {{ companyName }}
        </v-card-title>

        <v-card-subtitle class="case-card__subtitle">
            {{ description }}
        </v-card-subtitle>

        <v-card-actions>
            <v-btn
                color="blue lighten-2"
                text

                @click="show = !show"
            >
                View Case
                <v-icon>{{ show ? 'mdi-chevron-down' : 'mdi-chevron-right' }}</v-icon>
            </v-btn>

            <v-spacer></v-spacer>
        </v-card-actions>

        <v-expand-transition>
            <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Numquam, sunt nostrum. Unde, libero rem voluptates corrupti necessitatibus modi minima,
                    maiores cum animi eligendi amet vel, saepe corporis magnam praesentium similique?
                </v-card-text>
            </div>
        </v-expand-transition>
    </v-card>
</template>

<script>

export default {
    name: 'case-block',

    props: {
        imageUrl: {
            type: String,
            default: null,
        },
        companyName: {
            type: String,
            default: null,
        },
        description: {
            type: String,
            default: null,
        },
        gridRow: {
            type: String,
            default: '1',
        },
        gridColumn: {
            type: String,
            default: '1',
        },
    },

    data: () => ({
        show: false,
    }),

}
</script>

<style lang="scss">

.case-card {
        // importants here are used to overwrite default font sizes of vuetify cards
    &__title {
        font-family: Arial;
        font-size: 1rem !important;
        font-weight: bold;
    }

    &__subtitle {
        font-size: 2rem !important;
    }
}

</style>
