<template>
    <v-navigation-drawer
        v-model="opened"
        absolute
        color="#000"
        width="100%"
    >
        <v-btn
            text
            dark
            class="menu-close"
            @click="opened = false"
        >
            <v-icon>mdi-close</v-icon>
        </v-btn>
        <v-list class="menu">
            <v-list-item-group
                v-model="selectedItem"
                class="menu__item-group"
                active-class="deep-purple--text"
            >
                <v-list-item v-for="item in items"
                             :key="item.id"
                             class="menu__item"
                >
                    <v-list-item-title class="menu__item-title">
                        <span class="float-right"> {{ item.text }} </span>
                    </v-list-item-title>
                </v-list-item>
            </v-list-item-group>
        </v-list>
    </v-navigation-drawer>
</template>

<script>

// Data
import menuItems from '../data/menuItems.json'

export default {
    name: 'menu-items',

    props: {
        opened: {
            type: Boolean,
            default: false,
        },
    },

    data: () => ({
        selectedItem: null,
        items: menuItems,
    }),
}

</script>

<style lang="scss">

.menu {
    margin-left: 40px;
    &__item-group {
        display: block;
        v-list-item {
        }
    }
    &__item {
        border-bottom: 0.5px solid #a3a3a3;
        &-title {
            color: #fff !important;
            font-size: 110px !important;
        }

    }
}

.menu-close {
    position: absolute;
}

.triangle {
    border-style: solid;
    border-width: 20px 0 20px 30px;
    border-color: transparent transparent transparent #ffff;
}

</style>
