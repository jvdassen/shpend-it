<script>
import conf from './conf.json'
export default {
  data() {
    return conf
  },
  async mounted() {
    window.app = this
  },
  computed: {
    deductedMoneys() {
      var total = 0
      var deductions = this.items.forEach(e => {
        var ded = parseInt(e.deduction) || 0
        total += ded
      })
      var deducted = this.richdude.moneys - total
      if (deducted <= 0) {
        return 'You did it!'
      } return `CHF ${new Number(deducted).toLocaleString()}`
    }
  },
  methods: {
    sell: function (item) { 
      if(item.deduction >= item.cost) {
        item.deduction -= item.cost
      }
    },
    buy: function (item) {
      item.deduction += item.cost
    }
  }
}
</script>

<template>
<div>
  <div class="rich">
    <div class="iconwrap">
      <div class="icon" :style="{backgroundImage: 'url(/' + richdude.img +')'}"></div>
    </div>
    <h2 class="name">Spend {{richdude.name}} Money</h2>
  </div>
  <h2 class="moneys">{{deductedMoneys}}</h2>
  <div class="stuffs">
    <div class="stuff" v-for="(item, index) in items">
      <div class="iconproductwrap">
        <div class="iconproduct" :style="{backgroundImage: 'url(/' + item.img +')'}"></div>
      </div>
      <h3 class="title">{{item.name}}</h3>
      <h4 class="cost">CHF {{item.cost}}</h4>
      <div class="controls">
        <button @click="sell(item)">Sell</button>
        <input class="quant" v-model="item.deduction" type="number" name="Amount" min="1" >
        <button @click="buy(item)">Buy</button>
      </div>
    </div>
  </div>

</div>
</template>
