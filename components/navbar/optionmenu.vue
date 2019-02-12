<template>
    <div>
        <v-layout column fill-height>
            <v-flex > <div class="line"></div></v-flex>
            <v-flex md6>
                <v-layout row fill-height align-center >
                    <v-flex xs3></v-flex>
                    <v-flex v-for="item in config" :key="item">
                        <h3>{{item}}</h3>
                    </v-flex>
                    <v-flex xs3></v-flex>
                </v-layout>
            </v-flex>
        </v-layout>
    </div>
</template>

<script>
export default {
    props:['config'],
    data(){
        return{

        }
    }

}
</script>

<style lang="stylus">
    .line
        background black
        width 100%
        height 3px
        border-width 10px
        border-color black
</style>
