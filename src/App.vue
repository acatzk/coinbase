<template>
  <div id="app">
    <nav-bar />
    <main>
      <section class="container mx-auto max-w-7xl sm:px-4 pt-6 pb-8">
        <div class="bg-white sm:rounded border shadow-sm">
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
        <div class="flex flex-wrap mt-5">
          <div class="w-full sm:w-1/2">
            <div class="bg-white rounded border border-b shadow-sm">
              <div class="border-b flex justify-between">
                <h3 class="text-blue-400 px-6 py-4 text-lg font-medium">Your Potfolio</h3>
                <div class="flex space-x-3 text-sm mr-4">
                  <button class="font-medium py-4 text-blue-400 border-b border-blue-400 focus:outline-none">
                    List
                  </button>
                  <button class="font-medium py-4 text-gray-400 border-b border-transparent hover:border-gray-400 focus:outline-none transition">
                    Chart
                  </button>
                </div>
              </div>
              <!-- First row -->
              <div class="flex items-center px-6 py-6 text-gray-500 text-lg border-b" v-for="(item, i) in portfolio" :key="i">
                <div class="w-1/4 flex items-center">
                  <div class="inline-flex rounded-full">
                    <svg  :class="`w-9 h-9 text-white ${item.color}`" 
                          fill="currentColor"  
                          xmlns:xlink="http://www.w3.org/1999/xlink"  
                          xmlns="http://www.w3.org/2000/svg"  
                          viewBox="0 0 20 20"  
                          preserveAspectRatio="xMidYMid meet"> 
                      <path xmlns="http://www.w3.org/2000/svg" 
                            fill-rule="evenodd"  
                            d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.736 6.979C9.208 6.193 9.696 6 10 6c.304 0 .792.193 1.264.979a1 1 0 001.715-1.029C12.279 4.784 11.232 4 10 4s-2.279.784-2.979 1.95c-.285.475-.507 1-.67 1.55H6a1 1 0 000 2h.013a9.358 9.358 0 000 1H6a1 1 0 100 2h.351c.163.55.385 1.075.67 1.55C7.721 15.216 8.768 16 10 16s2.279-.784 2.979-1.95a1 1 0 10-1.715-1.029c-.472.786-.96.979-1.264.979-.304 0-.792-.193-1.264-.979a4.265 4.265 0 01-.264-.521H10a1 1 0 100-2H8.017a7.36 7.36 0 010-1H10a1 1 0 100-2H8.472c.08-.185.167-.36.264-.521z"  
                            clip-rule="evenodd"> 
                      </path> 
                    </svg>
                  </div>
                  <span class="ml-2">{{ item.title }}</span>
                </div>
                <div class="w-1/4 flex items-center">
                  <div  class="rounded-full h-2 flex-grow bg-orange-500"
                        v-show="item.title === 'Bitcoin'">
                  </div>
                  <div  v-if="item.title !== 'Bitcoin'" :class="item.title !== 'Bitcoin' ? item.color : ''">&bull;</div>
                  <span class="ml-2">{{ item.percentage }}</span>
                </div>
                <div class="w-1/4 text-right">
                  <div class="text-right">
                    {{ item.decimalValue }}
                  </div>
                </div>
                <div class="w-1/4">
                  <div class="text-gray-400 text-right">
                   {{ item.covertedValue }}
                  </div>
                </div>
              </div>
              <div class="py-4 text-md">
                <div class="text-center text-gray-500">
                  <span>Total Balance = CA$21.34</span>
                </div>
              </div>
            </div>
          </div>
          <!-- Recent Activity -->
          <div class="sm:w-1/2 pl-0 sm:pl-4 flex mt-10 sm:mt-0 w-full">
            <div class="bg-white rounded border shadow-sm flex-1">
              <div class="border-b">
                <h3 class="text-blue-400 px-6 py-4 text-lg font-medium">Recently Activity</h3>
              </div>
              <div>
                <div class="text-center px-6 py-8 space-y-2">
                  <div>
                    <svg  class="h-16 w-16 inline-block text-gray-400" 
                          fill="currentColor" 
                          xmlns:xlink="http://www.w3.org/1999/xlink" 
                          xmlns="http://www.w3.org/2000/svg" 
                          viewBox="0 0 24 24" 
                          preserveAspectRatio="xMidYMid meet">
                      <path xmlns="http://www.w3.org/2000/svg" 
                            d="M17.604.012a.603.603 0 00-.416.175l-4.493 4.485a.9.9 0 01-1.263.002L6.939.236a.603.603 0 00-.841-.002L.31 5.871c-.2.194-.311.457-.311.733v5.34c0 .271.11.533.305.726l11.277 11.144a.603.603 0 00.846 0L23.695 12.67c.194-.193.305-.454.305-.727V6.605c0-.27-.107-.528-.299-.72L18.04.189a.603.603 0 00-.435-.177zM6.615 2.5a.292.292 0 01.2.084l8.138 8.047a2.19 2.19 0 010 3.119l-2.43 2.4a.293.293 0 01-.408 0l-8.14-8.046a2.172 2.172 0 01-.65-1.561c0-.59.23-1.143.648-1.557l2.431-2.402a.292.292 0 01.211-.084zm11.15.707a2.241 2.241 0 01.278.022c.5.067.955.327 1.312.68l2.57 2.542a.284.284 0 010 .404l-3.91 3.868a.29.29 0 01-.41 0l-4-3.955a.285.285 0 010-.407l2.54-2.51a2.241 2.241 0 011.62-.644zm4.087 6.123a.29.29 0 01.341.283v1.705h-.002c0 .2-.08.39-.222.532l-9.28 9.306a.686.686 0 01-.511.225.743.743 0 01-.533-.227l-.655-.613a.284.284 0 01-.008-.41L21.697 9.412a.287.287 0 01.155-.082zm-19.424.106c.1.016.197.062.281.144l7.5 7.322c.13.13.35.396.35.717 0 .205-.047.495-.27.717l-.002-.002-.531.477a.445.445 0 01-.604-.014l-7.064-6.899a.917.917 0 01-.277-.658V9.951c0-.348.317-.566.617-.515z">
                      </path>
                    </svg>
                  </div>
                  <p class="text-2xl text-gray-500">No buys or sell yet</p>
                  <p class="text-gray-500 max-w-xs mx-auto">You've successfully linked a payment method and can start buying digital currency.</p>
                  <div>
                    <button class="bg-blue-500 text-white py-4 px-6 rounded border">
                      Buy now
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
    <footer class="mt-10 bg-white font-medium text-gray-400">
      <div class="container max-w-7xl mx-auto py-3 px-4">
        <div class="flex items-center flex-wrap  justify-between">
          <div>
            <a href="#" class="inline-block text-gray-400 px-2 py-2 rounded hover:bg-black-20 transition">Home</a>
            <a href="#" class="inline-block text-gray-400 px-2 py-2 rounded hover:bg-black-20 transition">Careers</a>
            <a href="#" class="inline-block text-gray-400 px-2 py-2 rounded hover:bg-black-20 transition">Legal & Privacy</a>
          </div>
          <div class="flex items-center space-x-2 text-sm">
            <div>&copy; 2020 Coinbase</div>
            <select class="rounded text-sm focus:outline-none">
              <option>English</option>
            </select>
            <div>
              <button class="block rounded text-sm font-medium bg-blue-500 text-white py-2 px-2 focus:ring-2 focus:ring-blue-300">
                Need Help?
              </button>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
  export default {
    name: 'app',
    props: {},
    components: {
      NavBar: () => import('@/components/NavBar')
    },
    data () { 
      return {
        portfolio: [
          {
            icon: '<svg  class="w-8 h-8 text-white" fill="currentColor"  xmlns:xlink="http://www.w3.org/1999/xlink"  xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 20 20"  preserveAspectRatio="xMidYMid meet"> <path xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd"  d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.736 6.979C9.208 6.193 9.696 6 10 6c.304 0 .792.193 1.264.979a1 1 0 001.715-1.029C12.279 4.784 11.232 4 10 4s-2.279.784-2.979 1.95c-.285.475-.507 1-.67 1.55H6a1 1 0 000 2h.013a9.358 9.358 0 000 1H6a1 1 0 100 2h.351c.163.55.385 1.075.67 1.55C7.721 15.216 8.768 16 10 16s2.279-.784 2.979-1.95a1 1 0 10-1.715-1.029c-.472.786-.96.979-1.264.979-.304 0-.792-.193-1.264-.979a4.265 4.265 0 01-.264-.521H10a1 1 0 100-2H8.017a7.36 7.36 0 010-1H10a1 1 0 100-2H8.472c.08-.185.167-.36.264-.521z"  clip-rule="evenodd"> </path> </svg>',
            title: 'Bitcoin',
            percentage: '100%',
            decimalValue: '0.0010BTC ',
            covertedValue: 'CAD$21.28',
            color: 'text-orange-500'
          },
          {
            icon: '<svg  class="w-8 h-8 text-white" fill="currentColor"  xmlns:xlink="http://www.w3.org/1999/xlink"  xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 20 20"  preserveAspectRatio="xMidYMid meet"> <path xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd"  d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.736 6.979C9.208 6.193 9.696 6 10 6c.304 0 .792.193 1.264.979a1 1 0 001.715-1.029C12.279 4.784 11.232 4 10 4s-2.279.784-2.979 1.95c-.285.475-.507 1-.67 1.55H6a1 1 0 000 2h.013a9.358 9.358 0 000 1H6a1 1 0 100 2h.351c.163.55.385 1.075.67 1.55C7.721 15.216 8.768 16 10 16s2.279-.784 2.979-1.95a1 1 0 10-1.715-1.029c-.472.786-.96.979-1.264.979-.304 0-.792-.193-1.264-.979a4.265 4.265 0 01-.264-.521H10a1 1 0 100-2H8.017a7.36 7.36 0 010-1H10a1 1 0 100-2H8.472c.08-.185.167-.36.264-.521z"  clip-rule="evenodd"> </path> </svg>',
            title: 'Litecoin',
            percentage: '0%',
            decimalValue: '0.0000 LTC',
            covertedValue: 'CAD$0.00',
            color: 'text-gray-500'
          },
          {
            icon: '<svg  class="w-8 h-8 text-white" fill="currentColor"  xmlns:xlink="http://www.w3.org/1999/xlink"  xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 20 20"  preserveAspectRatio="xMidYMid meet"> <path xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd"  d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.736 6.979C9.208 6.193 9.696 6 10 6c.304 0 .792.193 1.264.979a1 1 0 001.715-1.029C12.279 4.784 11.232 4 10 4s-2.279.784-2.979 1.95c-.285.475-.507 1-.67 1.55H6a1 1 0 000 2h.013a9.358 9.358 0 000 1H6a1 1 0 100 2h.351c.163.55.385 1.075.67 1.55C7.721 15.216 8.768 16 10 16s2.279-.784 2.979-1.95a1 1 0 10-1.715-1.029c-.472.786-.96.979-1.264.979-.304 0-.792-.193-1.264-.979a4.265 4.265 0 01-.264-.521H10a1 1 0 100-2H8.017a7.36 7.36 0 010-1H10a1 1 0 100-2H8.472c.08-.185.167-.36.264-.521z"  clip-rule="evenodd"> </path> </svg>',
            title: 'Ethereum',
            percentage: '0%',
            decimalValue: '0.0000 ETH',
            covertedValue: 'CAD$0.00',
            color: 'text-indigo-500'
          }
        ]
      } 
    }
  }
</script>
