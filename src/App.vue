<template>
    <div class="container">
        <app-header :maxQuotes='10'  :quoteCount='quotes.length'></app-header>
    <app-new-quote @newQuoteAdded='add'></app-new-quote>
        <app-quote-grid :quotes='quotes' @delteQuote='delteQuote'></app-quote-grid>
        <div class='row'>
            <div class='col-sm-12 text-center'>
                <div class='alert alert-info'>
                    click on quote to delete it
                </div>
            </div>
    </div>
    
    </div>
</template>

<script>
    import quoteGrid from './components/quoteGrid'
     import newQuote from './components/newQuote'
     import Header from './components/header'
    export default {
        data:function(){
          return{
              maxQuotes : 10,
            
              quotes:['starting Quote'],
        
              
          }  
          
        },
        methods:{
          add(quote){
              if(this.quotes.length >= this.maxQuotes)
                  {
                    return   alert('delete some quotes');
                  }
              
              this.quotes.push(quote);
          },
          delteQuote(index){
           
              this.quotes.splice(index,1);
          }
        },
        components:{
            appQuoteGrid: quoteGrid,
            appNewQuote: newQuote,
            appHeader: Header
        }
    }
</script>

<style>
</style>
