<template>
   <div class="container">
      <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
      <div  class="column">
         <app-new-quote @quoteAdded="newQuote"></app-new-quote>
      </div>
      <div id="greeting" class="column">
         <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
         <div class="delete_text"></div>
         <div class="row">
         </div>
      </div>
   </div>
</template>
<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue';
import Header from './components/Header.vue';
export default {
	data: function() {
		return {
			quotes: ['A note, just for you:'],
			maxQuotes: 10
		}
	},
	methods: {
		newQuote(quote) {
			if (this.quotes.length >= this.maxQuotes) {
				return alert('Max of 10 lines of text reached. Please delete a line of text first before moving forward.')
			}
			this.quotes.push(quote);
		},
		deleteQuote(index) {
			this.quotes.splice(index, 1);
		}
	},
	components: {
		appQuoteGrid: QuoteGrid,
		appNewQuote: NewQuote,
		appHeader: Header
	}
}
</script>

<style>
.delete_text {
  background-color: #f2f2f2;
  padding: 30px;
  text-align: center;
  font-size: 22px;
  font-family: 'Muli', sans-serif;
  margin-top: 20px;
}
.column {
    float: left;
    width: 50%;
}

/* Clear floats after the columns */
.row:after {
    content: "";
    display: table;
    clear: both;
}

#greeting {
  margin-top: 80px;
  padding-top: 35px;
  width: 45%;
  margin-left: 40px;
  background-image: url('http://pngimage.net/wp-content/uploads/2018/06/notepad-background-png-1.png');
  background-size: cover;
}
</style>
