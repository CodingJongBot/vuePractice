<template>
    <li>{{ name }}?!</li>
    
</template>

<script>
export default {
    props:{
        name:{
            type: String,
            default:''
        }

        
    },
}
</script>


<style scoped lang="scss">
    h1{
        color:yellow !important;
    }

</style>
