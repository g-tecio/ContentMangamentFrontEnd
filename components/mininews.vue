import components from '../.nuxt/components/nuxt-child';
<template>
    <div>
        <v-layout column fill-height>
            <v-flex v-for="item in config" :key="item">
                <v-layout row fill-height style="width:100%;">
                    <v-flex >
                    </v-flex>
                    <v-flex xs12>
                        <!-- <v-layout fill-height> -->
                            <v-card flat style="width:100%">
                                <v-card-title >
                                    <v-layout column justify-center >
                                        <v-flex>
                                            <div class="headline">{{item.title}}</div>
                                        </v-flex>
                                        <div style="height:10px"></div>
                                        <v-flex>
                                            <dates :config="item.dates"></dates>
                                        </v-flex>
                                    </v-layout>
                                </v-card-title>
                            </v-card>
                        <div class="linevmn"></div>
                        <!-- </v-layou> -->
                    </v-flex>
                </v-layout>
            </v-flex>
        </v-layout>
    </div>
</template>

<script>
import dates from '~/components/dates'
export default {
    props:['config'],
    data(){
        return{
        }
    },
    components:{
        dates
    }
}
</script>

<style lang="stylus">

.linevmn
    background black
    height 1px
    margin-left 5%
    width 90%
    border-width 10px
    border-color black
    margin-bottom 5px
</style>
