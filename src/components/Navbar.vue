<template>
    
<nav class="fixed top-0 z-50 w-full bg-white border-b border-gray-200 dark:bg-gray-800 dark:border-black-700">
  <div class="px-3 py-3 lg:px-5 lg:pl-3">
    <div class="flex items-center justify-between">
      <div class="flex items-center justify-start">
        <a href="/" class="flex ml-2 md:mr-24">
          <img src="../assets/img/logo.jpg" class="h-10 mr-2" alt="" />
          <span class="self-center text-xl font-semibold sm:text-2xl whitespace-nowrap dark:text-white">Neko</span>
        </a>
        <center>
        <div>
    <div v-if="isAuthenticated">
    </div>
    <div v-if="isAuthenticated">
      <a @click="logout" class="text-white cursor-pointer bg-green-700 hover:bg-green-800 focus:ring-4 focus:outline-none focus:ring-green-300 font-medium rounded-lg text-sm px-4 py-2 text-center mr-3 md:mr-0 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800">Logout</a>
    </div>
    <div v-else>
      <a href="/login" class="text-white bg-green-700 hover:bg-green-800 focus:ring-4 focus:outline-none focus:ring-green-300 font-medium rounded-lg text-sm px-4 py-2 text-center mr-3 md:mr-0 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800">Login</a>
    </div>
    </div>
  </center>
      </div>
            </div>
          </div>
          
</nav>
   

  </template>
  
  <script>
  import store from '../store';
  import { mapActions, mapGetters } from 'vuex';
  
    export default {
      computed: {
        ...mapGetters('auth', ['isAuthenticated']),
      },
      methods: {
        ...mapActions('auth', ['logout'])
      },
    }
  </script>