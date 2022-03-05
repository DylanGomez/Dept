<template>
    <v-container fluid class="case-container">
        <case-block
            v-for="customerCase in cases"
            :key="customerCase.id"
            :company-name="customerCase.company"
            :description="customerCase.title"
            :image-url="customerCase.img"
            :grid-row="customerCase.gridRow"
            :grid-column="customerCase.gridColumn"
        >
        </case-block>
    </v-container>
</template>

<script>

import CaseBlock from '../components/CaseBlock.vue'
import data from '../data/db.json'

export default {
    name: 'home',

    components: {
        CaseBlock,
    },

    data() {
        return {
            cases: data,
        }
    },
}
</script>

<style lang="scss">
.case-container {
    display: grid;
    gap: 2rem;
    grid-template-columns: 1fr 1fr 1fr 1fr;
}

</style>
