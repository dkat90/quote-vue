<template id="">
  <div class="row">
    <appQuote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{ quote }}</appQuote>
  </div>
</template>

<script type="text/javascript">
  import Quote from "./Quote.vue"
  export default {
    props: ['quotes'],
    components:{
      appQuote: Quote
    },
    methods: {
      deleteQuote(index){
        this.$emit('quoteDeleted', index);
      }
    }
  }
</script>

<style media="screen">

</style>
