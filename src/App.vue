<template>
  <div id="app">
    <router-view/>
                <v-snackbar :color="snackColor" v-model="snackVisible" :timeout="4000" top right>
                {{ snackText }}
            </v-snackbar>
            <v-dialog v-model="rsvp" >
                <v-card>
                    <v-card-title>
                        R S V P
                        <v-spacer></v-spacer>
                        <v-btn @click="rsvp = false">Close</v-btn>
                    </v-card-title>
                    <v-card-text>
                        <v-flex class="xs8 offset-xs3 hidden-sm-and-down">
                            <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScHqm4CcEhY5MP4EpmRCuT_Vu2l8dufbi70rJU9MR1zuJYoIQ/viewform?embedded=true" :width="800" height="1104" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

                        </v-flex>

                        <v-flex class="xs12 hidden-md-and-up">
                            <iframe src="https://docs.google.com/forms/d/e/1FAIpQLScHqm4CcEhY5MP4EpmRCuT_Vu2l8dufbi70rJU9MR1zuJYoIQ/viewform?embedded=true" :width="300" height="1104" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>

                        </v-flex>
                    </v-card-text>
                </v-card>
            </v-dialog>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
