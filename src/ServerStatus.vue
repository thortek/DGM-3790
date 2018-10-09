<template>
<div class="single_element">
<p>Server Status: {{ status }}</p>
<button @click="changeStatus">Change to Normal</button>
<button id="critical" @click="changeStatusAgain">Change to Critical</button>
</div>
</template>

<script>
    export default {
        data: function() {
            return {
                status: 'Critical'
            }
            
        },
        methods: {
            changeStatus() {
                this.status = 'Normal';
            },
            changeStatusAgain() {
                this.status = 'Critical';
            }
        }
    }
</script>

<style>
button {
  padding-top: 10px;
  padding-bottom: 10px;
  padding-right: 20px;
  padding-left: 20px;
  border: none;
  background-color: #6ba6d7;
  color: #fff;
  font-size: 16px;
}
button:hover {
  background-color: #3376ad;
  border: none;
  cursor: pointer;
}
#critical {
    margin-left: 10px;
}
p {
  font-family: 'Source Code Pro', monospace;
}
.single_element {
  background-color: #f4f4f4;
  padding-top: 5px;
  padding-bottom: 25px;
  padding-left: 25px;
  border: solid 1px #94b3cc;
}
</style>
