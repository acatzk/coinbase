<template>
  <header>
    <!-- Top navigation -->
    <div class="bg-blue-600">
      <div class="container mx-auto max-w-7xl px-4">
        <div class="flex items-center justify-between flex-wrap py-4">
          <div class="block sm:hidden">
            <button class="block focus:outline-none focus:ring-2 focus:ring-blue-300 rounded-sm">
              <svg  class="w-8 h-8 text-white"
                    stroke="currentColor" 
                    xmlns:xlink="http://www.w3.org/1999/xlink" 
                    xmlns="http://www.w3.org/2000/svg" 
                    viewBox="0 0 24 24" 
                    preserveAspectRatio="xMidYMid meet">
                <path xmlns="http://www.w3.org/2000/svg" 
                      stroke-linecap="round" 
                      stroke-linejoin="round" 
                      stroke-width="1.5" 
                      d="M4 6h16M4 12h16M4 18h16">
                </path>
              </svg>
            </button>
          </div>
          <div class="text-white text-2xl">cointbase</div>
          <div class="flex-shrink-0">
            <div class="focus:outline-none rounded-full block">
              <div class="sm:flex sm:items-center">
                <div>
                  <img class="inline-block w-8 h-8 rounded-full" src="@/assets/avatar.jpg" alt="">
                </div>
                <div class="ml-1 hidden sm:flex sm:items-center">
                  <span class="text-white font-medium text-sm">Joshua Galit</span>
                  <div class="ml-1">
                    <svg  class="w-4 h-4 block text-white opacity-50" 
                          fill="currentColor" 
                          xmlns:xlink="http://www.w3.org/1999/xlink" 
                          xmlns="http://www.w3.org/2000/svg" 
                          viewBox="0 0 20 20" 
                          preserveAspectRatio="xMidYMid meet">
                      <path xmlns="http://www.w3.org/2000/svg" 
                            fill-rule="evenodd" 
                            d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" 
                            clip-rule="evenodd">
                      </path>
                    </svg>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Secondary Navigation -->
    <nav class="hidden sm:block sm:bg-white bg-blue-600 sm:border-b">
      <div class="container mx-auto max-w-7xl border-b px-4">
        <div class="sm:flex -mx-px sm:space-x-5">
          <a href="#" class="flex items-center sm:border-b text-gray-200 sm:border-blue-400 py-4">
            <svg  class="w-5 h-5 block text-gray-200 sm:text-blue-400" 
                  fill="currentColor" 
                  xmlns:xlink="http://www.w3.org/1999/xlink" 
                  xmlns="http://www.w3.org/2000/svg" 
                  viewBox="0 0 20 20" 
                  preserveAspectRatio="xMidYMid meet">
              <path xmlns="http://www.w3.org/2000/svg" 
                    d="M3 4a1 1 0 011-1h12a1 1 0 011 1v2a1 1 0 01-1 1H4a1 1 0 01-1-1V4zm0 6a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H4a1 1 0 01-1-1v-6zm11-1a1 1 0 00-1 1v6a1 1 0 001 1h2a1 1 0 001-1v-6a1 1 0 00-1-1h-2z">
              </path>
            </svg>
            <span class="ml-1 text-gray-200 sm:text-blue-400">Dashboard</span>
          </a>
          <a href="#" class="flex items-center border-b border-transparent hover:border-gray-400 py-4">
            <svg  class="w-5 h-5 block text-gray-300 sm:text-gray-400" 
                  fill="currentColor" 
                  xmlns:xlink="http://www.w3.org/1999/xlink" 
                  xmlns="http://www.w3.org/2000/svg" 
                  viewBox="0 0 20 20" 
                  preserveAspectRatio="xMidYMid meet">
              <path xmlns="http://www.w3.org/2000/svg" 
                    d="M8 5a1 1 0 100 2h5.586l-1.293 1.293a1 1 0 001.414 1.414l3-3a1 1 0 000-1.414l-3-3a1 1 0 10-1.414 1.414L13.586 5H8zm4 10a1 1 0 100-2H6.414l1.293-1.293a1 1 0 10-1.414-1.414l-3 3a1 1 0 000 1.414l3 3a1 1 0 001.414-1.414L6.414 15H12z">
              </path>
            </svg>
            <span class="ml-1 text-gray-300 sm:text-gray-400">Buy/Sell</span>
          </a>
          <a href="#" class="flex items-center border-b border-transparent hover:border-gray-400 py-4">
            <svg  class="w-5 h-5 block text-gray-300 sm:text-gray-400" 
                  fill="currentColor" 
                  xmlns:xlink="http://www.w3.org/1999/xlink" 
                  xmlns="http://www.w3.org/2000/svg" 
                  viewBox="0 0 20 20" 
                  preserveAspectRatio="xMidYMid meet">
              <path xmlns="http://www.w3.org/2000/svg" 
                    d="M4 4a2 2 0 00-2 2v1h16V6a2 2 0 00-2-2H4z">
              </path>
              <path xmlns="http://www.w3.org/2000/svg" 
                    fill-rule="evenodd" 
                    d="M18 9H2v5a2 2 0 002 2h12a2 2 0 002-2V9zM4 13a1 1 0 011-1h1a1 1 0 110 2H5a1 1 0 01-1-1zm5-1a1 1 0 100 2h1a1 1 0 100-2H9z" 
                    clip-rule="evenodd">
              </path>
            </svg>  
            <span class="ml-1 text-gray-300 sm:text-gray-400">Account</span>
          </a>
          <a href="#" class="flex items-center border-b border-transparent hover:border-gray-400 py-4">
            <svg  class="w-5 h-5 block text-gray-300 sm:text-gray-400" 
                  fill="currentColor" 
                  xmlns:xlink="http://www.w3.org/1999/xlink" 
                  xmlns="http://www.w3.org/2000/svg" 
                  viewBox="0 0 20 20" 
                  preserveAspectRatio="xMidYMid meet">
              <path xmlns="http://www.w3.org/2000/svg" 
                    fill-rule="evenodd" 
                    d="M6 6V5a3 3 0 013-3h2a3 3 0 013 3v1h2a2 2 0 012 2v3.57A22.952 22.952 0 0110 13a22.95 22.95 0 01-8-1.43V8a2 2 0 012-2h2zm2-1a1 1 0 011-1h2a1 1 0 011 1v1H8V5zm1 5a1 1 0 011-1h.01a1 1 0 110 2H10a1 1 0 01-1-1z" 
                    clip-rule="evenodd">
              </path>
              <path xmlns="http://www.w3.org/2000/svg" 
                    d="M2 13.692V16a2 2 0 002 2h12a2 2 0 002-2v-2.308A24.974 24.974 0 0110 15a24.98 24.98 0 01-8-1.308z">
              </path>
            </svg>
            <span class="ml-1 text-gray-300 sm:text-gray-400">Tools</span>
          </a>
          <a href="#" class="flex items-center border-b border-transparent hover:border-gray-400 py-4">
            <svg  class="w-5 h-5 block text-gray-300 sm:text-gray-400" 
                  fill="currentColor" 
                  xmlns:xlink="http://www.w3.org/1999/xlink" 
                  xmlns="http://www.w3.org/2000/svg" 
                  viewBox="0 0 20 20" 
                  preserveAspectRatio="xMidYMid meet">
              <path xmlns="http://www.w3.org/2000/svg" 
                    d="M8 5a1 1 0 100 2h5.586l-1.293 1.293a1 1 0 001.414 1.414l3-3a1 1 0 000-1.414l-3-3a1 1 0 10-1.414 1.414L13.586 5H8zm4 10a1 1 0 100-2H6.414l1.293-1.293a1 1 0 10-1.414-1.414l-3 3a1 1 0 000 1.414l3 3a1 1 0 001.414-1.414L6.414 15H12z">
              </path>
            </svg>
            <span class="ml-1 text-gray-300 sm:text-gray-400">Settings</span>
          </a>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
  export default {
    name: 'header',
    data () {
      return {
        toggle: false
      }
    }
  }
</script>