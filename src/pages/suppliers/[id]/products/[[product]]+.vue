<template>
  <div>
    <template v-if="route.params.product">
      <h2>
        Product {{ route.params.product.join(' > ') }}
      </h2>
    </template>
    <template v-else>
      <h2>All products</h2>
      <ul>
        <li><router-link :to="{ name: '/suppliers/[id]/products/[[product]]+', params: { id: route.params.id, product: ['1'] } }">Example productcategory</router-link></li>
        <li><router-link :to="{ name: '/suppliers/[id]/products/[[product]]+', params: { id: route.params.id, product: ['1', '2'] } }">Example product</router-link></li>
      </ul>
    </template>
  </div>
</template>

<script setup lang="ts">
  const route = useRoute()
  console.log(route.params.id, route.params.product)
</script>
