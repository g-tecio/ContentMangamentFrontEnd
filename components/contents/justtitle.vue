<template>
    <div>
        <v-card flat>
            <v-layout row>
                <div>
                    <v-card-title>
                        <v-layout column>
                            <div class="headline">
                                {{config.title}} 
                            </div>
                            <br>
                            <div><dates :config="config.dates"></dates></div>
                        </v-layout>
                    </v-card-title>
                    <v-card-actions>
                        <minidate style="color:blue" :config="config.minidate"></minidate>
                        <v-spacer></v-spacer>
                        <div>
                            <span><nuxt-link to="/new">See More...</nuxt-link></span>
                        </div>
                    </v-card-actions>
                </div>
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
