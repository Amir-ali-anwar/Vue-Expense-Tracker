<template>
  <Header></Header>
  <div class="container">
    <Balance />
    <IncomeExpenses />
    <TransactionList :transactions="transactions" />
    <AddTransaction />
  </div>
</template>
<script setup>
import Header from './components/Header.vue'
import Balance from './components/Balance.vue';
import IncomeExpenses from './components/IncomeExpenses.vue';
import TransactionList from './components/TransactionList.vue'
import AddTransaction from './components/AddTransaction.vue'
const transactions = [
  { id: 1, text: 'Flower', amount: -19.90 },
  { id: 2, text: 'Salary', amount: 219.90 },
  { id: 2, text: 'Book', amount: 219.90 },
  { id: 2, text: 'Camera', amount: 1500 },
]

</script>
<style ></style>