<template>
    <div>
      <nav class="bg-white dark:bg-gray-900 fixed w-full z-20 top-0 left-0 border-b border-gray-200 dark:border-gray-600">
        <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
          <a href="https://flowbite.com/" class="flex items-center">
            <img src="../assets/img/logoc.webp" class="h-8 mr-3" alt="Flowbite Logo">
            <span class="self-center text-2xl font-semibold whitespace-nowrap text-yellow-900">Cheesecuit</span>
          </a>
          <div class="flex md:order-2">

            <div v-if="isAuthenticated">
              <router-link to="/cart-checkout" class="relative inline-flex items-center mr-4 px-5">
              <router-link to="/cart" class="relative inline-flex items-center mr-4 px-5">
    
              
              </router-link>
             </router-link>
  
            </div>
            <div v-if="isAuthenticated" class="flex md:order-2">
                 <CartBadgeComponent/>
              <div >
                <a @click="logout"
                  class="text-white  cursor-pointer bg-blue-700 hover:bg-yellow-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2 text-center mr-3 -top-9 md:mr-0  dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Logout</a>
              </div>
            </div>
            <button data-collapse-toggle="navbar-sticky" type="button"
              class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
              aria-controls="navbar-sticky" aria-expanded="false">
              <span class="sr-only">Open main menu</span>
              <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
                <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M1 1h15M1 7h15M1 13h15" />
              </svg>
            </button>
          </div>
          <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1" id="navbar-sticky">
            <ul
              class="flex flex-col p-4 md:p-0 mt-4 font-medium border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 text-yellow-900">
              <li>
                <a href="/"
                  class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-yellow-400 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text-yellow-900">Home</a>
              </li>
              <li>
                <a href="/produk"
                  class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-yellow-400 md:p-0 md:dark:hover:text-yellow-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text-yellow-900">Produk</a>
              </li>
              <li>
                <a href="/categories"
                  class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-yellow-400 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text-yellow-900">Kategori</a>
              </li>
              <li>
                <a href="/brand"
                  class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-yellow-400 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text-yellow-900">Brand</a>
              </li>
              <li>
                <a href="/contact"
                  class="block py-2 pl-3 pr-4 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:hover:text-yellow-400 md:p-0 md:dark:hover:text-blue-500 dark:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text-yellow-900">Kontak</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </div>
  </template>
    
    <script>
    import { mapActions, mapGetters } from 'vuex';
    import CartBadgeComponent from './CartBadgeComponent.vue';
    export default {
      computed: {
            ...mapGetters('auth', ['isAuthenticated']),
        },
        methods: {
            ...mapActions('auth', ['logout']),
        },
        components: { CartBadgeComponent }
    };
    </script>