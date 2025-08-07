<template>
  <div>
    <h1>Supplier {{ route.params.id }}</h1>
    <router-view />
  </div>
</template>
<script setup lang="ts">
  const route = useRoute()
  console.log(route.params.id)

  // eslint-disable-next-line @typescript-eslint/consistent-type-imports
  type RouteNamesForThisFilePath = import('vue-router/auto-routes')._RouteNamesForFilePath<'src/pages/suppliers/[id].vue'>;
  const route2 = useRoute<RouteNamesForThisFilePath>();
</script>
