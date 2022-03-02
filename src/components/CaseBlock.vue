<template>
    <v-card
        class="mx-auto"
        max-width="344"
    >
        <v-img
            :src="require(`../assets/Images/${imageUrl}`)"
            height="200px"
        ></v-img>

        <v-card-title>
            {{ companyName }}
        </v-card-title>

        <v-card-subtitle>
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
        cols: {
            type: Number,
            default: 6,
        },
    },

    data: () => ({
        show: false,
    }),

}
</script>

<style lang="scss">

</style>
