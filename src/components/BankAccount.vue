<template>
<h2>Account Type: {{type}}</h2>
  <h2>Amount: {{ money }}</h2>
  <h2>Account: {{ state ? 'Enabled' : 'Disabled' }}</h2>
  <div v-for="(service, index) in services" :key="index">
      {{index+1}} - {{ service }}
  </div>
  <balance-action 
    text = 'Add'
    @action="addMoney"
  />
  <balance-action
    text = 'Decrease'
    @action="decreaseMoney"
    :disable="disable"
  />
</template>

<script>
import BalanceAction from './BalanceAction'

export default {
    name: 'BankAccount',
    components: { 
        BalanceAction
    },
    data() {
        return {
            money: 1000,
            type: 'Visa',
            state: true,
            disable: false,
            services: ['Payments', 'Money Transfers', 'Bank Transfers']
        }
    },
    methods: {
        addMoney() {
            this.money += 100
            this.disable = false
        },
        decreaseMoney () {
            this.money -= 100
            if(this.money === 0){
                this.disable = true
                alert('No money available')
                return
            }
        }
    }
}
</script>

<style>

</style>