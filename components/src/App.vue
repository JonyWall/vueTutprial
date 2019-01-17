<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <app-header></app-header>
            </div>
        </div>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <servers-list :servers="servers" :selectServer="selectServer"></servers-list>
            </div>
            <div class="col-xs-12 col-sm-6">
                <app-server-details :selectedServer="servers[selectedServer]"></app-server-details>
            </div>
        </div>
        <hr>
        <div class="row">
            <div class="col-xs-12">
                <footer>
                    <p>All Servers are managed here</p>
                </footer>
            </div>
        </div>
    </div>
</template>

<script>
  import ServersList from './ServersList';
  import Header from './Header'
  import ServerDetails from './ServerDetails'
  export default  {
      components: {
        ServersList,
        'app-header': Header,
        'app-server-details': ServerDetails
      },
      data: function() {
            return {
                servers: [
                  {id: 1, status: 'Normal'},
                  {id: 2, status: 'Critical'},
                  {id: 3, status: 'Normal'},
                  {id: 4, status: 'Unknown'},
                  {id: 5, status: 'Normal'}
                ],
                selectedServer: null
            }
      },
      methods: {
            selectServer(id) {
                this.selectedServer = id-1;
            }
      }

  }

</script>

<style>

</style>
