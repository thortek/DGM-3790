<template>
    <div class="">
        <ul class="">
            <li
                    class=""
                    v-for="index in 5">
                Server #{{ index }}
            </li>
        </ul>
    </div>
</template>

<script>
</script>

<style scoped>
    div {
        border: 1px solid blue;
    }
</style>
