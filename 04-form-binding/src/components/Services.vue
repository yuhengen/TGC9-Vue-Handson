<template>
  <div>
    <h1>Price of Services (HANDS ON 5.2)</h1>
    <form>
      <div>
        <label>Services</label>
        <div>
          <input type="checkbox" v-model="services" value="song" />Birthday Song
          ($3.00)
        </div>
        <div>
          <input type="checkbox" v-model="services" value="cake" />Birthday Cake
          ($20.00)
        </div>
        <div>
          <input type="checkbox" v-model="services" value="mascot" />Animal
          Mascot ($30.00)
        </div>
        <div>
          <input type="checkbox" v-model="services" value="gift" />Special
          Door-Gift for each child ($5.00)
        </div>
      </div>
      <br />
      <div>
        <h1>Total Cost: ${{ totalCost }}</h1>
        <span>Selected Services: {{ services }}</span>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      services: [],
    };
  },
  computed: {
    //   totalCost: function(){
    //       let totalPrice = 0;
    //       if (this.services.includes('song')){
    //           totalPrice += 3;
    //       }
    //       if (this.services.includes('cake')){
    //           totalPrice += 20;
    //       }
    //       if (this.services.includes('mascot')){
    //           totalPrice += 30;
    //       }
    //       if (this.services.includes('gift')){
    //           totalPrice += 5;
    //       }
    //       return totalPrice
    //   }

    totalCost: function () {
      let costTable = {
        song: 3,
        cake: 20,
        mascot: 30,
        gift: 5,
      };
      let total = 0;
      for (let selectedService of this.services) {
        total = total + costTable[selectedService];
      }
      return total;
    },
  },
};
</script>

<style scoped>
.margin-space {
  margin-top: 30px;
}
</style>