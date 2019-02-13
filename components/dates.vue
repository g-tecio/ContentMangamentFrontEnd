<template>
    <div>
        <div>
            <span style="color:red">Read</span>
            <span>| {{config.words}} |</span> 
            <span>{{config.date}}</span> 
        </div>
    </div>
</template>

<script>
export default {
    props:['config']

}
</script>

<style>

</style>
