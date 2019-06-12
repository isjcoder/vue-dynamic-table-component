<template>
  <div id="app">
    <section class="section">
      <div class="container">
        <div class="has-text-centered">
          <div>
            <img width="25%" src="./assets/logo.png">
          </div>
          <div>
            <h2 class="title">Dynamic table component with Vue</h2>
          </div>
        </div>
        <br>

        <DynamicTable/>
      </div>
    </section>
  </div>
</template>

<script>
import DynamicTable from "./components/DynamicTable";
import "bulma/css/bulma.css";

export default {
  name: "App",
  components: {
    DynamicTable
  }
};
</script>
