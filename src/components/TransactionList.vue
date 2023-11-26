<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <li :class="transaction.amount < 0 ? 'minus' : 'plus'" v-for="transaction in transactions" :key="transaction.id">
      {{ console.log({transaction})
       }}
      <p v-if="transaction.length>0">
       {{ transaction.text }} <span>{{ transaction.amount }}</span><button class="delete-btn" @click="deleteTransaction(transaction.id)">x</button></p>
       <p v-else>No Transaction to Show</p>
      </li>
  </ul>
</template>
<script setup>
import {defineProps} from 'vue'
const emit = defineEmits(['transactionDeleted']);
const props = defineProps({
  transactions: {
    type: Array,
    required: true,
  },
});
const deleteTransaction=(id)=>{
  emit('transactionDeleted',id)
}
</script>