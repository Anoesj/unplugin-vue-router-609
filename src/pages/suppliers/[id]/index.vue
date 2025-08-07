<template>
  <ul>
    <li><router-link :to="{ name: '/suppliers/[id]/products/[[product]]+', params: { id: $route.params.id } }">Products</router-link></li>
    <li><router-link :to="{ name: '/suppliers/[id]/results/[[version]]', params: { id: $route.params.id } }">Results</router-link></li>
  </ul>
</template>
