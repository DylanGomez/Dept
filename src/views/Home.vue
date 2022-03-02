<template>
    <div>
        <case-block
            v-for="customerCase in cases"
            :key="customerCase.id"
            :company-name="customerCase.company"
            :description="customerCase.title"
            :image-url="customerCase.img"
        >
        </case-block>
    </div>
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
