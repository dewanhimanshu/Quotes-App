<template>
<div class='row'>
    <app-quote v-for="(quote,index) in quotes" @click.native='deleteQuote(index)'>{{quote}}</app-quote>
    
    </div>

</template>


<script>
    import Quote from './quote'
    export default{
        props:['quotes'],
        components:{
            appQuote: Quote
        },
        methods:{
            deleteQuote(index){
                this.$emit('delteQuote',index);
            }
        }
        
    }


</script>



<style>


</style>