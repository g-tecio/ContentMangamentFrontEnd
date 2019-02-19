<template>
    <div>
        <v-card flat>
            <v-layout row>
                <div>
                    <v-card-title>
                        <v-layout column>
                            <div class="fonttitle">
                                {{config.title}} 
                            </div>
                            <div><dates :config="config.dates"></dates></div>
                            <div class="fontlitle">{{config.content}}</div>
                        </v-layout>
                    </v-card-title>
                    <v-card-actions>
                        <minidate style="color:blue" :config="config.minidate"></minidate>
                        <v-spacer></v-spacer>
                        <div>
                            <span><a href="">See More...</a></span>
                        </div>
                    </v-card-actions>
                </div>
                <slot name="line" class="spacedos"></slot>
            </v-layout>
        </v-card>
    </div>
</template>

<script>
import dates from '~/components/dates'
import minidate from '~/components/minidate'

export default {
    props:['config'],
    components:{
        dates,
        minidate
    }
}
</script>

<style lang="stylus">
    .fontlitle
        font-size 13px
    .fonttitle
        font-size 23px
    .spacedos
        padding 5px
</style>
