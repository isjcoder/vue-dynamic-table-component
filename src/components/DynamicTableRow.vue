<template>
  <tr>
    <td>
      <input class="input" type="text" placeholder="Enter item name">
    </td>
    <td>
      <button class="button is-danger" @click="removeRow(index)" v-show="index>0">
        <font-awesome-icon icon="trash-alt"/>
      </button>
    </td>
  </tr>
</template>

<script>
export default {
  name: "DynamicTableRow",
  props: {
    item: Object,
    items: Array,
    index: Number
  },
  data() {
    return {
      loading: true
    };
  },
  methods: {
    removeRow(index) {
      this.$delete(this.items, index);
    }
  }
};
</script>
