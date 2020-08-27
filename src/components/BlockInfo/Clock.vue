<template>
    <div class="mx-auto my-card">
        <v-row justify="center">
        <AnalogClock :size="200"
        backgroundImage="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1545553805386&di=ec656215a2958d617ef30631e96304e0&imgtype=0&src=http%3A%2F%2Fimg1.ali213.net%2Fshouyou%2Fupload%2Fimage%2F2018%2F07%2F09%2F584_2018070952816881.png"
    /> </v-row>
    </div>
</template>

<script>
import {AnalogClock} from 'vue-analog-clock'
export default {
    components: {AnalogClock}
}
</script>

<style lang="scss" scoped>
</style>