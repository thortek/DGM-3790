<template>
    <div class="layout">
        <p>Server Status: <b>{{ status }}</b></p>
        <button @click="changeStatus">Change Status</button>
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
            }
        }
    }
</script>

<style scoped>
.layout {
    background-color: #f1f1f1;
    padding-top: 1px;
    padding-bottom: 20px;
    padding-left: 20px;
    padding-right: 20px;
    margin-top: 20px;
    border: solid 1px #202b3e;
}
</style>