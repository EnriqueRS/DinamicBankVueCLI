<template>
<h2>Account Type: {{type}}</h2>
  <h2>Saldo: {{ money }}</h2>
  <h2>Account: {{ state ? 'Enabled' : 'Disabled' }}</h2>
  <div v-for="(item, index) in services" :key="index">
      {{index+1}} - {{ item }}
  </div>
  <balance-action 
    text = 'Add'
    @action="addMoney"
  />
  <balance-action
    text = 'Decrease'
    @action="decreaseMoney"
  />
</template>

<script>
import BalanceAction from './BalanceAction'

export default {
    name: 'BankAccount',
    data() {
        return {
            money: 1000,
            type: 'Visa',
            'state': true,
            services: ['Payments', 'Money Transfers', 'Bank Transfers']
        }
    },
    components: { 
        BalanceAction
    },
    methods: {
        addMoney() {
            this.money += 100
        },
        decreaseMoney () {
            this.money -= 100
        }
    }
}
</script>

<style>

</style>