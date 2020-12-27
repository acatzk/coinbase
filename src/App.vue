<template>
  <div id="app">
    <nav-bar />
    <main>
      <section class="container mx-auto max-w-7xl sm:px-4 pt-6 pb-8">
        <div class="bg-white border-t border-b sm:border-r sm:border-l sm:rounded shadow">
          <div class="border-b px-6">
            <div class="flex justify-between -mb-px">
              <div class="sm:hidden block font-semibold text-blue-400 self-center">
                Price Charts
              </div>
              <div class="hidden sm:flex space-x-4">
                <button class="py-4 text-blue-400 border-b border-blue-400 focus:outline-none">
                  Bitcoin &middot; CA$21,380.01
                </button>
                <button class="py-4 text-gray-400 border-b border-transparent hover:border-gray-400 focus:outline-none transition">
                  Ethereum &middot; CA$884.80
                </button>
                <button class="py-4 text-gray-400 border-b border-transparent hover:border-gray-400 focus:outline-none transition">
                  Litecoin &middot; CA$358.24
                </button>
              </div>
              <div class="flex space-x-3 text-sm">
                <button class="py-4 text-gray-400 border-b border-transparent hover:border-gray-400 focus:outline-none transition">
                  1H
                </button>
                <button class="py-4 text-gray-400 border-b border-transparent hover:border-gray-400 focus:outline-none transition">
                  1D
                </button>
                <button class="py-4 text-gray-400 border-b border-transparent hover:border-gray-400 focus:outline-none transition">
                  1W
                </button>
                <button class="py-4 text-blue-400 border-b border-blue-400 focus:outline-none">
                  1M
                </button>
                <button class="py-4 text-gray-400 border-b border-transparent hover:border-gray-400 focus:outline-none transition">
                  1Y
                </button>
                <button class="py-4 text-gray-400 border-b border-transparent hover:border-gray-400 focus:outline-none transition">
                  All
                </button>
              </div>
            </div>
          </div>
          <div class="flex items-center sm:hidden px-6">
            <div class="flex-1 py-6 ">
              <div class="text-gray-500 mb-2">
                <span class="text-3xl align-top">CA$</span>
                <span class="text-5xl">21,404</span>
                <span class="text-3xl align-top">.74 </span> 
              </div>
              <div class="text-green-400 text-sm">
                &uarr; CAD$12,955.35(154.16%)
              </div>
            </div>
            <div>
              <select class="block w-full rounded focus:outline-none appearance-none text-gray-500 border border-gray-400">
                <option>BTC</option>
                <option>ETH</option>
                <option>LTC</option>
              </select>
            </div>
          </div>
          <div class="hidden sm:flex">
            <div class="w-1/3 text-center py-6 ">
              <div class="border-r">
                <div class="text-gray-500 mb-2">
                  <span class="text-3xl align-top">CA$</span>
                  <span class="text-5xl">21,404</span>
                  <span class="text-3xl align-top">.74 </span> 
                </div>
                <div class="uppercase text-gray-400 tracking-wider">
                  Bitcoin Price
                </div>
              </div>
            </div>
            <div class="w-1/3 text-center py-6 ">
              <div class="border-r">
                <div class="text-gray-500 mb-2">
                  <span class="text-3xl align-top">
                    <span class="text-green-400">+</span>  CA$
                  </span>
                  <span class="text-5xl">12,998</span>
                  <span class="text-3xl align-top">.48</span> 
                </div>
                <div class="uppercase text-gray-400 tracking-wider">
                  Since last month (CAD)
                </div>
              </div>
            </div>
            <div class="w-1/3 text-center py-6">
              <div class="text-gray-500 mb-2">
                <span class="text-3xl align-top">
                  <span class="text-green-400">+</span>
                </span>
                <span class="text-5xl">154.99</span>
                <span class="text-3xl align-top">%</span> 
              </div>
              <div class="uppercase text-gray-400 tracking-wider">
                Since last month (%)
              </div>
            </div>
          </div>
        </div>
        
      </section>
    </main>
  </div>
</template>

<script>
  export default {
    name: 'app',
    props: {},
    components: {
      NavBar: () => import('@/components/NavBar')
    },
    data () { return {} }
  }
</script>
