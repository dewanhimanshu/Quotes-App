<template>
<div class='row'>
<form>
    <div class='col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group'>
    <label>Quote</label>
    <textarea class='form-control' rows='3' v-model='quote'></textarea>
    </div>
    <div class='col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group'>
      <button class='btn btn-default' @click.prevent='newQuote'>AddQuote</button>
    </div>
    
</form>
    </div>

</template>


<script>
  
    export default{
        data:function(){
            return{
                quote:''
            }
        },
        methods:{
            newQuote(){
                this.$emit('newQuoteAdded',this.quote);
            }
        }
    
    }


</script>



<style>


</style>