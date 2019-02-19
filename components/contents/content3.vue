<template>
    <div>
        <v-card flat>
            <v-layout column>
                <div>
                    <v-img 
                    :src="config.img"
                    aspect-ratio=1
                    max-height="150px"
                    width="250px"
                    ></v-img>
                </div>
                <div>
                    <v-card-title>
                        <v-layout column>
                            <div class="headline">
                                {{config.title}} 
                            </div>
                            <div><dates :config="config.dates"></dates></div>
                            <div>{{config.content}}</div>
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
                <slot name="line"></slot>
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
    .linevnf
        background black
        width 1px
        height 250px
        border-width 1px
        border-color black
        margin 15px
</style>
