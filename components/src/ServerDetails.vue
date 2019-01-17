<template>
    <div>
      <p v-if="selectedServer">Selected server id: {{selectedServer.id}}, status={{selectedServer.status}}</p>
      <p v-else>Please select server</p>
      <hr>
      <button @click="ChangeStatus"> Change Status </button>
    </div>
</template>

<script>
    export default {
        props: ['selectedServer'],
        methods: {
            ChangeStatus() {
                this.selectedServer.status = "Normal";
            }
        }
    }
</script>

<style scoped>
    p {
      border: 1px solid red;
    }
</style>
