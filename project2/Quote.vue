<template>
   <div class="quotetext">
       <div class="text">
       <div class="text-body quote">
<slot></slot>
      </div>
   </div>
   </div>
</template>
<script>
</script>
<style>
.text-body {
    font-family: 'Indie Flower', cursive;
    font-size: 26px;
    font-style: italic;
    color: #3a3a3a;
    text-align: left;
    padding-left: 60px;
    padding-right: 25px;
}

.quote {
    cursor: pointer;
}

.quote:hover {
    background-color: #ffe2e2;
}
</style>