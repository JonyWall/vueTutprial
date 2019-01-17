<template>
      <li @click="selectServer(server.id)">Server #{{ server.id }} status: {{ server.status }}</li>
</template>

<script>
    export default {
        props: ['server', 'selectServer']
    }
</script>

<style scoped>

</style>
