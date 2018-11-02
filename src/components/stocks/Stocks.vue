<template>
  <div>
    <app-stock v-for="stock in stocks" :stock="stock"></app-stock>
  </div>
</template>

<script>
import appStock from './Stock.vue';
  export default {
    components: {
      appStock
    },
    computed: {
      stocks() {
        return this.$store.getters.stocks;
      }
    }
  }
</script>