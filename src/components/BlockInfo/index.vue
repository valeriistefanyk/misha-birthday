<template>
    <v-container grid-list-lg>
        <v-layout row wrap>
            <v-flex>
                <clock></clock>
            </v-flex>
            <v-flex>
                <geo></geo>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
import Clock from './Clock';
import Geo from './Geo';
    export default {
        components: {
            Clock,
            Geo,
        }
    }
</script>

<style lang="scss" scoped>

</style>