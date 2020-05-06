<template>
    <div class="container mt-5">
        <progressBar :quotesCount="quotes.length" :maxQuotes="maxQuotes"></progressBar>
        <insertQuote @onQuoteAdded="newQuote"></insertQuote>
        <quotes :quotes="quotes" @onQuoteDelete="deleteQuote"></quotes>
    </div>
</template>

<script>
    import ProgressBar from "./components/ProgressBar";
    import InserQuote from "./components/InserQuote";
    import Quotes from "./components/Quotes";
    export default {
        data() {
            return {
                quotes: ['initial'],
                maxQuotes: 5
            }
        },
        methods: {
            //llega automaticamente
            newQuote(quote) {
                if(this.quotes.length >= this.maxQuotes) {
                    return alert('Max reached, delete a quote');
                } else {
                    this.quotes.push(quote);
                }
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1);
            }
        },
        components: {
            progressBar: ProgressBar,
            insertQuote: InserQuote,
            quotes: Quotes
        },
    }
</script>

<style>

</style>
