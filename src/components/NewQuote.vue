<template>
   <div class="row">
      <form>
         <div id="form_input">
            <h2>Note Creator</h2>
      <form> 
      <textarea rows="3" v-model="quote" placeholder="What do you want to say?"></textarea><br><br>
      
      <button class="btn" @click.prevent="createNew">Add Line of Text</button>
      <button class="btn-ins" onclick="return confirm('Are you sure you wish to delete your entire note and start over?')">Delete Entire Note</button>
      <h3>Select Your Signature</h3>
      <div class="select" style="width:200px;">
      <select v-model="quote">
      <option value="" disabled selected>Select signature</option>
      <option @click.prevent="createNew" value="Love ,">Love ,</option>
      <option @click.prevent="createNew" value="Yours truly ,">Yours truly ,</option>
      <option @click.prevent="createNew" value="With warm regards ,">With warm regards ,</option>
      <option @click.prevent="createNew" value="Sincerely ,">Sincerely ,</option>
      <option @click.prevent="createNew" value="Never call me ,">Never call me ,</option>
      <option @click.prevent="createNew" value="Leave me alone ,">Leave me alone ,</option>
      </select>
      </div>
      </form>  
      </div>
      </form>
   </div>
</template>

<script>
    export default {
        data: function() {
            return {
                quote: ''
            };
        },
        methods: {
            createNew() {
                this.$emit('quoteAdded', this.quote);
                this.quote = '';
            }

        }
    }
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Charmonman');

#form_input {
  max-width: 800px;
  width: 100%;
  
}

#form_input textarea {
    width: 100%;
    border: solid 3px #00a5ed;
    border-radius: 25px;
    padding: 30px;
    font-family: 'Muli', sans-serif;
    font-size: 25px;
}
button {
    background-color: #40aa33;
    padding-top: 20px;
    padding-bottom: 20px;
    padding-left: 30px;
    padding-right: 30px;
    color: #fff;
    font-family: 'Muli', sans-serif;
    font-size: 20px;
    border-radius: 20px;
    margin-bottom: 30px;
}

.btn-ins {
    background-color: #ff0000;
    padding-top: 20px;
    padding-bottom: 20px;
    padding-left: 30px;
    padding-right: 30px;
    color: #fff;
    font-family: 'Muli', sans-serif;
    font-size: 20px;
    border-radius: 20px;
    margin-bottom: 30px;
    margin-left: 20px;
}

h2 {
    font-family: 'Muli', sans-serif;
    font-size: 40px;
    text-align: left;
}

h5 {
    font-family: 'Muli', sans-serif;
    font-size: 22px;
    text-align: right;
    text-decoration: underline;
}
p {
    text-align: right;
}
</style>

