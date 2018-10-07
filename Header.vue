<template>
      <div class="lines">
    <h3>Single Lines of Text Added</h3>
    <div class="w3-border">
  <div class="w3-blue" style="height:35px;" :style="{width: (quoteCount / maxQuotes) * 100 + '%'}">
      {{ quoteCount }} / {{ maxQuotes }}
  </div>
</div>
<p>To delete a line, simply click on the that line.</p>
    </div>
</template>
<script>
export default {
    props: ['quoteCount', 'maxQuotes']
}
</script>

<style>
.w3-blue {
    padding-left: 20px;
    padding-top: 6px;
}
</style>
