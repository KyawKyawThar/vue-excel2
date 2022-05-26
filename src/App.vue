<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png" />
    <div class="container mb-5">
      <div class="row">
        <div class="col-8 offset-2">
          <div class="text-left mt-3">
            <p>Upload a csv and and map the columns:</p>
            <vue-csv-import v-model="csv" :map-fields="['Name', 'Age', 'and']">
              <vue-csv-map :auto-match="true"></vue-csv-map>
            </vue-csv-import>
            <div class="mt-3">
              <div class="card" v-if="csv">
                <div class="card-body">
                  <pre>
                  {{ csv }}
                  </pre>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueCsvImport from "vue-csv-import";

export default {
  name: "App",
  components: {
    VueCsvImport,
  },
  data() {
    return {
      csv: null,
    };
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>\
