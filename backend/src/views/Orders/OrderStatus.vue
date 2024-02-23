<template>
  <span class="text-white py-1 px-2 rounded " :class="{
      'bg-emerald-500': ['created', 'completed'].includes(order.status),
      'bg-orange-400': order.status === 'process',
      'bg-red-500': order.status === 'cancelled',
      'bg-gray-400': order.status === 'created',
    }">{{ order.status }}</span>
</template>

<script setup>
const {order} = defineProps({
  order: Object
})
</script>

<style scoped>

</style>
