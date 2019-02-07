<template>
     <div>
        <v-navigation-drawer
            v-model="config.drawer"
            app
            floating
            persistent
            mobile-break-point="9091"
            width="260"
        >
            <v-list class="pa-1">
                <v-list-tile avatar>
                    <v-list-tile-content>
                        <v-toolbar-title>{{config.title}}</v-toolbar-title>
                    </v-list-tile-content>
                </v-list-tile>
            </v-list>

            <v-list class="pt-0" dense>
            <v-divider></v-divider>
    
            <v-list-tile
                v-for="item in config.items"
                :key="item.title"
                @click=""
            >
                <v-list-tile-action>
                <v-icon>{{ item.icon }}</v-icon>
                </v-list-tile-action>
    
                <v-list-tile-content>
                <v-list-tile-title>{{ item.title }}</v-list-tile-title>
                </v-list-tile-content>
            </v-list-tile>
            </v-list>
        </v-navigation-drawer>
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
