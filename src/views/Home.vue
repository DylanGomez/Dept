<template>
    <div>
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
        <v-container fluid class="client-container">
            <v-container class="text-center client-container__inner-container mb-5">
                <h2>Clients</h2>
                <span>We value a great working relationship with our clients above all else. It’s why they often come to our parties.
                    It’s also why we’re able to challenge and inspire them to reach for the stars.</span>
            </v-container>
            <v-container fluid class="client-container__logos">
                <client-block
                    v-for="client in clients"
                    :key="client.id"
                    :image-url="client.img"
                >
                </client-block>
            </v-container>
        </v-container>
    </div>
</template>

<script>
// Components
import CaseBlock from '../components/CaseBlock.vue'
import ClientBlock from '../components/ClientBlock.vue'

// Data
import casesJSON from '../data/cases.json'
import clientsJSON from '../data/clients.json'

export default {
    name: 'home',

    components: {
        CaseBlock,
        ClientBlock,
    },

    data() {
        return {
            cases: casesJSON,
            clients: clientsJSON,
        }
    },
}
</script>

<style lang="scss">

.case-container {
    display: grid;
    gap: 2rem;
    grid-template-columns: 20% 20% 20% 20%;
    justify-content: center;
}

@media only screen and (max-width: 768px) {
    .case-container {
        display: block;
        width: 90%;
    }
}

.client-container {
    background-color: #f3f6f6;

    &__inner-container {
        width: 560px;

        h2 {
            font-size: 60px;
        }

        span {
            width: 50px;
            font-family: Arial;
            font-size: 17px;
            line-height: 1.59;
        }
    }

    &__logos {
        display: grid;
        gap: 1rem;
        grid-template-columns: 1fr 1fr 1fr 1fr;
    }
}

@media only screen and (max-width: 768px) {
    .client-container {

        &__inner-container {
            width: 100vw;
        }

        &__logos {
            gap: 1rem;
            grid-template-columns: 50% 50%;
        }
    }
}

</style>
