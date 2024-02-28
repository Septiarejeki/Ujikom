<template>
  <section class="h-screen bg-gray-100 py-12 sm:py-16 lg:py-20">
  <div class="mx-auto px-4 sm:px-6 lg:px-8">
    <div class="flex items-center justify-center">
     <a href="/cheseecuit_kategori"> <h1 class="text-2xl font-semibold text-yellow-900">Menu Cheesecuit</h1></a>
     
    </div>

    <div class="mx-auto mt-8 max-w-4xl md:mt-12 lg:grid-cols-5">
      <div class="bg-white shadow">
        <div class="px-4 py-6 sm:px-8 sm:py-10">
          <div class="flow-root">
            <ul class="-my-8">
              <li class="flex flex-col space-y-3 py-6 text-left sm:flex-row sm:space-x-5 sm:space-y-0">
                <div class="shrink-0">
                  <img class="h-24 w-24 max-w-full rounded-lg object-cover" src="../assets/img/tiramisu.jpg" alt="" />
                </div>

                <div class="relative flex flex-1 flex-col justify-between">
                  <div class="sm:col-gap-5 sm:grid sm:grid-cols-2">
                    <div class="pr-8 sm:pr-5">
                      <p class="text-base font-bold text-gray-900 text-yellow-900">Cheesecuit Tiramisu </p>
                      <p class="mx-0 mt-1 font-semibold mb-0 text-sm text-gray-800 text-yellow-800">$259.00</p>
                    </div>

                  

                  </div>
                </div>
              </li>

              <li class="flex flex-col space-y-3 py-6 text-left sm:flex-row sm:space-x-5 sm:space-y-0">
                <div class="shrink-0">
                  <img class="h-24 w-24 max-w-full rounded-lg object-cover" src="../assets/img/strawberry.webp" alt="" />
                </div>

                <div class="relative flex flex-1 flex-col justify-between">
                  <div class="sm:col-gap-5 sm:grid sm:grid-cols-2">
                    <div class="pr-8 sm:pr-5">
                      <p class="text-base font-bold text-gray-900 text-yellow-900">Cheesecuit Starwberry</p>
                      <p class="mx-0 mt-1 font-semibold mb-0 text-sm text-gray-800 text-yellow-900">$259.00</p>
                    </div>

                    <div class="mt-4 flex items-end justify-between sm:mt-0 sm:items-start sm:justify-end">
                      
                      <button class="flex items-center justify-center rounded-l-md bg-gray-200 px-4 transition hover:bg-black hover:text-white">
                        <svg xmlns="http://www.w3.org/2000/svg" class="mr-2 h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
        <path stroke-linecap="round" stroke-linejoin="round" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
      </svg>
                      </button>
                      <button class="flex items-center justify-center rounded-r-md bg-gray-200 px-4 transition hover:bg-black hover:text-white">+</button>
                      <button class="flex items-center justify-center rounded-r-md bg-gray-200 px-4 transition hover:bg-black hover:text-white">+</button>
                    </div>
                  </div>
                </div>
              </li>
              
              <li class="flex flex-col space-y-3 py-6 text-left sm:flex-row sm:space-x-5 sm:space-y-0">
                <div class="shrink-0">
                  <img class="h-24 w-24 max-w-full rounded-lg object-cover" src="../assets/img/greentea.webp" alt="" />
                </div>

                <div class="relative flex flex-1 flex-col justify-between">
                  <div class="sm:col-gap-5 sm:grid sm:grid-cols-2">
                    <div class="pr-8 sm:pr-5">
                      <p class="text-base font-bold text-gray-900 text-yellow-900">Cheesecuit Greentea</p>
                      <p class="mx-0 mt-1 font-semibold mb-0 text-sm text-gray-800 text-yellow-900">$259.00</p>
                    </div>

                    <div class="mt-4 flex items-end justify-between sm:mt-0 sm:items-start sm:justify-end">
                      <p class="shrink-0 w-20 text-base font-semibold text-gray-900 sm:order-2 sm:ml-8 ">$259.00</p>

                    </div>
                  </div>

                  <div class="sm:order-1">
                        <div class="mx-auto flex h-8 items-stretch text-gray-600 sm:text-right">
                          <button class="flex items-center justify-center rounded-l-md bg-gray-200 px-4 transition hover:bg-black hover:text-white sm:text-right">-</button>
                          <button class="flex items-center justify-center rounded-r-md bg-gray-200 px-4 transition hover:bg-black hover:text-white">+</button>
                          <button class="flex items-center justify-center rounded-r-md bg-gray-200 px-4 transition hover:bg-black hover:text-white">+</button>
                        </div>
                      </div>
                </div>
              </li>
              
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>



      
</section>

</template>