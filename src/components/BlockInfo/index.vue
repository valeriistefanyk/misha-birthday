<template>
    <v-container grid-list-lg>
        <v-layout row wrap>
            <v-flex xs12 sm6 md4>
                <geo></geo>
            </v-flex>
            <v-flex xs12 sm6 md4 align-self-center>
                <clock></clock>
            </v-flex>
            <v-flex xs12 sm6 md4>
                <calendar></calendar>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
import Clock from './Clock';
import Geo from './Geo';
import Calendar from './Calendar';

    export default {
        components: {
            Clock,
            Calendar,
            Geo,
        }
    }
</script>

<style lang="scss" scoped>

</style>