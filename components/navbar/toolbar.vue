<template>
    <div>
        <v-toolbar>
            <v-toolbar-items>
                <v-btn icon @click="config.drawer = !config.drawer"><v-icon> toc </v-icon></v-btn>
            </v-toolbar-items>
            <v-spacer></v-spacer>
                <div v-for="item in config.social">
                    <v-card
                    hover
                    flat
                    :img="item.img"
                    :to="item.link"
                    width="40px"
                    height="40px"
                    light
                    style="margin-left:10px">
                    </v-card>
                </div>
        </v-toolbar>
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

<style>

</style>
