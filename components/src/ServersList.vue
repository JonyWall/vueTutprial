<template>
  <ul class="list-group">
      <app-server-item v-for="server in servers" :server="server" :selectServer="selectServer"></app-server-item>
  </ul>
</template>

<script>
    import ServerItem from './ServerItem'
    export default {
        components: {
          'app-server-item': ServerItem
        },
        props: ['servers', 'selectServer'],
    }
</script>
