<template>

  <div id="nav">
    <nav class="flex justify-center space-x-4 p-4 bg-blue-300">
      <router-link to="/" class="font- px-3 py-2 text-gray-700 rounded-lg hover:bg-gray-100 hover:text-gray-900">Home</router-link>
      <router-link to="/about" class="font- px-3 py-2 text-gray-700 rounded-lg hover:bg-gray-100 hover:text-gray-900">About</router-link> 
      <router-link to="/login" class="font- px-3 py-2 text-gray-700 rounded-lg hover:bg-gray-100 hover:text-gray-900">Login</router-link>
      <router-link to="/register" class="font- px-3 py-2 text-gray-700 rounded-lg hover:bg-gray-100 hover:text-gray-900">Register</router-link>
    </nav>
    <router-view/>
  </div>

</template>

<script>


export default {
  name: 'App',
}
</script>