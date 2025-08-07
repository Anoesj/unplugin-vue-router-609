<template>
  <div>
    <template v-if="route.params.version">
      <h2>
        Result {{ route.params.version }}
      </h2>
    </template>
    <template v-else>
      <h2>All results</h2>
      <ul>
        <li><router-link :to="{ name: '/suppliers/[id]/results/[[version]]', params: { id: route.params.id, version: '1' } }">Example result 1</router-link></li>
        <li><router-link :to="{ name: '/suppliers/[id]/results/[[version]]', params: { id: route.params.id, version: '2' } }">Example result 2</router-link></li>
      </ul>
    </template>
  </div>
</template>

<script setup lang="ts">
  const route = useRoute()
  console.log(route.params.id, route.params.version)
</script>
