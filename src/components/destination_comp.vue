<template>
  <div id="destination-list-one">
    <div class="destination" v-for="dest in destinationListDiscount" :key="dest.id">
      <p>{{ dest.from }}</p>
      <p>{{ dest.to }}</p>
      <p>{{ dest.time }}</p>
      <p>{{ dest.distance }}</p>
      <p>{{ dest.price }}</p>
      <p>{{ dest.tickets }}</p>
      <button v-on:click="applyCuopon">Apply coupon</button>
    </div>
  </div>
</template>

<script>
//import destinations from "../views/Destinations";

export default {
  name: "destination_comp",
  //components: { destinations } ,
  data: function() {
    return {};
  },

  computed: {
    destinationList() {
      return this.$store.getters.destinations;
    },
    destinationListDiscount() {
      return this.$store.getters.destinationListDiscount;
    }
  },

  methods: {
    applyCuopon: function() {
      this.$store.commit("ApplyCoupon");
    }
  }

};
</script>


<style scoped>
.item {
  background: rgb(47, 255, 141);
  margin-bottom: 5px;
  padding: 3px 5px;
}

#comp-list-one {
  background: #d9b1ff;
  box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
  margin-bottom: 30px;
  padding: 10px 20px;
}

#comp-list-one ul {
  padding: 0;
}

#comp-list-one li {
  display: inline-block;
  margin-right: 10px;
  margin-top: 10px;
  padding: 20px;
  background: rgba(255, 255, 255, 0.7);
}

.price {
  font-weight: bold;
  color: #E8800C;
}
</style>