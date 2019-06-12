<template>
  <div class="hello">
    <table class="table is-fullwidth">
      <thead>
        <tr>
          <th width="93%">
            <abbr title="Item">Item Name</abbr>
          </th>
          <th width="2%">
            <button class="button">
              <font-awesome-icon icon="plus" @click="AddRow"/>
            </button>
          </th>
        </tr>
      </thead>
      <tbody>
        <DynamicTableRow v-for="(item, index) in items" :items="items" :item="item" :index="index" />
      </tbody>
    </table>
  </div>
</template>

<script>
import _ from "lodash";
import { items } from "./items.js";
import DynamicTableRow from "./DynamicTableRow";

export default {
  name: "DynamicTable",
  data() {
    return {
      items: _.cloneDeep(items())
    };
  },
  components: {
    DynamicTableRow
  },
  methods: {
    AddRow() {
      this.items.push(_.first(_.cloneDeep(items())));
    }
  }
};
</script>
