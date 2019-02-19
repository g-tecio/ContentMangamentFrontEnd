<template>
    <div>
        <v-layout column fill-height>
            <v-flex style="margin-left: 8%; margin-right:11%">
                <v-layout row fill-height align-center justify-center>
                    <!-- <v-flex xs3></v-flex> -->
                    <v-flex xs1 v-for="item in config" :key="item">
                        <v-btn class="buttontxt" small flat>
                            {{item}}
                        </v-btn>
                    </v-flex>
                    <!-- <v-flex xs3></v-flex> -->
                </v-layout>
            </v-flex>
        </v-layout>
        <v-flex>
            <div class="line"></div>
        </v-flex>
    </div>
</template>

<script>
export default {
    props:['config'],
    data(){
        return{
            
        }
    },
}
</script>

<style lang="stylus">
    .line
        background black
        width 100%
        height 3px
        border-width 10px
        border-color black
    .upper
        margin-bottom  -15px
    .buttontxt
        font-size 10px
        font-weight bold
        width 12px
</style>
