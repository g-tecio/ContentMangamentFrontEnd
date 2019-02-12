<template>
    <div>
        <v-toolbar
            height="50px"
            fixed
            flat
            >
            <v-toolbar-items>
                <v-btn icon @click="config.drawer = !config.drawer"><v-icon> toc </v-icon></v-btn>
                    <v-btn
                    :href="'/'"
                    flat>
                        <v-icon>home</v-icon>
                        <div>&nbsp</div>
                       home
                    </v-btn>
            </v-toolbar-items>
            <v-toolbar-title>
            </v-toolbar-title>
            <v-spacer></v-spacer>
                <div v-for="item in config.social">
                    <v-card
                    hover
                    flat
                    :img="item.img"
                    :to="item.link"
                    width="30px"
                    height="30px"
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
