<template>
    <div>
        <v-layout fill-height style="  margin:auto; margin-top:10px; margin-bottom:20px; width:90%; align-items:center;" row>
            <v-card flat >
                <div> 
                <v-card-title>
                    <v-layout column align-center justify-center>
                        <div class="headline">
                            {{title}} 
                        </div>
                        <div><dates :config="config.dates"></dates></div>
                        <div>{{content}}</div>
                    </v-layout>
                </v-card-title>
                <v-card-actions>
                    <v-icon>person</v-icon>
                </v-card-actions>
                </div>
            </v-card>
            <div>
                <v-img 
                :src="config.img"
                aspect-ratio=1
                max-height="400px"
                width="630px"
                ></v-img>
            </div>
            <slot name="line"></slot>
        </v-layout>
    </div>
</template>

<script>
export default {
    props:['config'],
    data(){
        return{
            title: 'Usually, you would use this character style for a main headline',
            content: 'Times are changing fast and whilst some of us were simply born into this meteoric times there are others who were not.'
        }
    }
}
</script>

<style>

</style>
