<template>
  <div>
    <h2>
      All suppliers
    </h2>
    <ul>
      <li><router-link :to="{ name: '/suppliers/[id]/', params: { id: '1' } }">Example supplier 1</router-link></li>
      <li><router-link :to="{ name: '/suppliers/[id]/', params: { id: '2' } }">Example supplier 2</router-link></li>
    </ul>
  </div>
</template>
