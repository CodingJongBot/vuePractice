<template>

    <h1 @click="increase">
        {{message}}
    </h1>
    <div v-if="message > 4">
        4보다 큽니다.
    </div>

    <ul>
        <Fruits 
            v-for="fruit in fruits"
            :key=fruit
            :name="fruit">
            {{fruit}}
        </Fruits>
    </ul>
    <!-- <HelloWorld/> -->
</template>


<script>
import HelloWorld from '~/components/HelloWorld'
import Fruits from '~/components/Fruits'


export default {
    components:{
        HelloWorld,
        Fruits
    },
    data() {
        return{
            message : 0,
            fruits: ['apple','banana','cherry']
        }        
    },
    methods:{
        increase(){
            this.message+=1
        }
    }

}
</script>


<style lang="scss">
    h1 {
        font-size : 50px;
        color : deeppink;
    }

    ul{
        li{
            font-size:40px;
        }
    }

</style>
