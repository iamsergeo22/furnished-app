<template>
  <div class="font-sans tw-flex tw-flex-col tw-opacity-90">


    <header class="tw-top-0 tw-left-0 tw-right-0 tw-bg-transparent tw-z-50">
      <nav
        class="tw-bg-transparent tw-px-4 lg:tw-px-8 lg:tw-mx-4 tw-pt-8 tw-pb-0 tw-flex tw-flex-row tw-justify-between tw-items-center">

        <div>
          <nuxt-link to="/">
            <h1 class="lg:tw-text-4xl tw-text-2xl tw-font-extrabold tw-text-black">
              BLOOMWOODINTERIORS
            </h1>
          </nuxt-link>
        </div>

        <div class="tw-flex tw-gap-4">
          <img src="../assets/Group.svg" alt="">
          <img src="../assets/Vector.svg" alt="">
        </div>


      </nav>

      <div class="tw-block lg:tw-hidden tw-px-4 tw-mt-4">
        <button @click="toggleMenu"
          class="tw-flex tw-items-center tw-px-3 tw-py-2 border tw-rounded tw-border-gray-500 hover:tw-border-gray-600">
          <svg class="tw-current-color tw-h-3 tw-w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" fill="gray" />
          </svg>
        </button>
      </div>


      <nav class="tw-bg-transparent  tw-px-4 tw-flex tw-flex-col lg:tw-flex-row tw-justify-between lg:tw-items-center">


        <ul
          class="tw-tracking-wide tw-px-2 tw-font-extrabold tw-w-full tw-block tw-flex-grow lg:tw-space-x-8 tw-space-y-6 lg:tw-space-y-0 lg:tw-flex lg:tw-flex-initial lg:tw-w-auto tw-mt-4 lg:tw-mt-0"
          :class="{ 'tw-block': isOpen, 'tw-hidden': !isOpen }">
          <li class="tw-mb-6 lg:tw-mb-0">
            <!-- <search-input /> -->
          </li>

          <li @click="closeMenu">
            <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
              class="text-black font-medium	hover:text-blue-800 text-md hover:no-underline">Our Story</nuxt-link>
          </li>


          <li @click="closeMenu">
            <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
              class="text-black font-medium	hover:text-blue-800 text-md hover:no-underline">Responsibility</nuxt-link>
          </li>


          <li @click="closeMenu">
            <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
              class="text-black font-medium	hover:text-blue-800 text-md hover:no-underline">Careers</nuxt-link>
          </li>

          <li @click="closeMenu">
            <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
              class="text-black font-medium	hover:text-blue-800 text-md hover:no-underline">Media</nuxt-link>
          </li>

          <li @click="closeMenu">
            <nuxt-link to="/" :class="$route.path === '/' ? 'active' : ''"
              class="text-black font-medium	hover:text-blue-800 text-md hover:no-underline">Investor</nuxt-link>
          </li>


          <li @click="closeMenu">
            <nuxt-link to="/contact" :class="$route.path === '/contact' ? 'active' : ''"
              class="text-black font-medium	hover:text-blue-800 text-md hover:no-underline">Contact Us</nuxt-link>
          </li>





        </ul>

        <div
          class="tw-bg-white tw-items-center tw-justify-between lg:tw-w-1/4 tw-flex tw-rounded-full tw-p-3 tw-mb-4"
          style="top: 5px">

          <v-text-field label="Search"></v-text-field>
          <!-- 
            <v-autocomplete v-model="selectedItem3" :items="items3" label="Item 3" /> -->
          <div class="bg-color tw-p-2 hover:tw-bg-blue-400 tw-cursor-pointer tw-mx-1 tw-rounded-full">

            <svg class="tw-w-6 tw-h-6 tw-text-black" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"
              fill="currentColor">
              <path fill-rule="evenodd"
                d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                clip-rule="evenodd" />
            </svg>

          </div>

        </div>

      </nav>

      <nav class="bg-color tw-flex tw-flex-row  tw-px-8 tw-gap-8 tw-py-2 tw-items-center"
      
      >

        <div class="tw-relative tw-inline-block tw-text-left">
          <!-- Dropdown button -->
          <button id="dropdownButton" data-dropdown-toggle="dropdown"
            class="tw-text-white tw-bg-transparent tw-hover:bg-blue-800 tw-focus:ring-4 tw-focus:outline-none tw-focus:ring-blue-300 tw-font-extrabold tw-rounded-lg tw-text-sm tw-px-5 tw-py-2.5 tw-text-center tw-inline-flex tw-items-center dark:tw-bg-transparent dark:tw-hover:bg-blue-700 dark:tw-focus:ring-blue-800"
            type="button">
            Furniture Collections
            <svg class="tw-w-2.5 tw-h-2.5 tw-ms-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
              viewBox="0 0 10 6">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="m1 1 4 4 4-4" />
            </svg>
          </button>


        </div>

        <div class="tw-relative tw-inline-block tw-text-left">
          <!-- Dropdown button -->
          <button id="dropdownButton" data-dropdown-toggle="dropdown"
            class="tw-text-white tw-font-extrabold tw-bg-transparent tw-hover:bg-blue-800 tw-focus:ring-4 tw-focus:outline-none tw-focus:ring-blue-300 tw-rounded-lg tw-text-sm tw-px-5 tw-py-2.5 tw-text-center tw-inline-flex tw-items-center dark:tw-bg-transparent dark:tw-hover:bg-blue-700 dark:tw-focus:ring-blue-800"
            type="button">
            Featured Categories
            <svg class="tw-w-2.5 tw-h-2.5 tw-ms-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
              viewBox="0 0 10 6">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="m1 1 4 4 4-4" />
            </svg>
          </button>


        </div>

        <div class="tw-relative tw-inline-block tw-text-left">
          <!-- Dropdown button -->
          <button id="dropdownButton" data-dropdown-toggle="dropdown"
            class="tw-text-white tw-bg-transparent tw-hover:bg-blue-800 tw-focus:ring-4 tw-focus:outline-none tw-focus:ring-blue-300 tw-font-extrabold tw-rounded-lg tw-text-sm tw-px-5 tw-py-2.5 tw-text-center tw-inline-flex tw-items-center dark:tw-bg-transparent dark:tw-hover:bg-blue-700 dark:tw-focus:ring-blue-800"
            type="button">
            Custom creations
            <svg class="tw-w-2.5 tw-h-2.5 tw-ms-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
              viewBox="0 0 10 6">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="m1 1 4 4 4-4" />
            </svg>
          </button>


        </div>

        <div class="tw-relative tw-inline-block tw-text-left">
          <!-- Dropdown button -->
          <button id="dropdownButton" data-dropdown-toggle="dropdown"
            class="tw-text-white tw-bg-transparent tw-hover:bg-blue-800 tw-focus:ring-4 tw-focus:outline-none tw-focus:ring-blue-300 tw-font-extrabold tw-rounded-lg tw-text-sm tw-px-5 tw-py-2.5 tw-text-center tw-inline-flex tw-items-center dark:tw-bg-transparent dark:tw-hover:bg-blue-700 dark:tw-focus:ring-blue-800"
            type="button">
            Limited editions
            <svg class="tw-w-2.5 tw-h-2.5 tw-ms-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
              viewBox="0 0 10 6">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="m1 1 4 4 4-4" />
            </svg>
          </button>


        </div>
        <div class="tw-relative tw-inline-block text-left">
          <!-- Dropdown button -->
          <button id="dropdownButton" data-dropdown-toggle="dropdown"
            class="tw-text-white tw-bg-transparent tw-hover:bg-blue-800 tw-focus:ring-4 tw-focus:outline-none tw-focus:ring-blue-300 tw-font-extrabold tw-rounded-lg tw-text-sm tw-px-5 tw-py-2.5 tw-text-center tw-inline-flex tw-items-center dark:tw-bg-transparent dark:tw-hover:bg-blue-700 dark:tw-focus:ring-blue-800"
            type="button">
            Best sellers
            <svg class="tw-w-2.5 tw-h-2.5 tw-ms-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
              viewBox="0 0 10 6">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="m1 1 4 4 4-4" />
            </svg>
          </button>


        </div>

        <div class="tw-relative tw-inline-block text-left">
          <!-- Dropdown button -->
          <button id="dropdownButton" data-dropdown-toggle="dropdown"
            class="tw-text-white tw-bg-transparent tw-hover:bg-blue-800 tw-focus:ring-4 tw-focus:outline-none tw-focus:ring-blue-300 tw-font-extrabold tw-rounded-lg tw-text-sm tw-px-5 tw-py-2.5 tw-text-center tw-inline-flex tw-items-center dark:tw-bg-transparent dark:tw-hover:bg-blue-700 dark:tw-focus:ring-blue-800"
            type="button">
            Seasonal picks
            <svg class="tw-w-2.5 tw-h-2.5 tw-ms-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none"
              viewBox="0 0 10 6">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="m1 1 4 4 4-4" />
            </svg>
          </button>


        </div>



      </nav>
    </header>



    <div class="tw-flex-grow">
      <Nuxt />
    </div>


    <footer class="tw-text-white tw-shadow-2xl tw-shadow-gray-900">
      <div class="tw-px-8 tw-flex tw-flex-col tw-gap-4 tw-justify-center tw-items-center">
        <h1 class="tw-text-4xl tw-font-extrabold tw-text-white tw-mt-8">
          BLOOMWOODINTERIORS
        </h1>
        <p class="tw-text-xl tw-font-medium tw-text-white tw-text-center">Sign up for exclusive Product Offers and Sale Dates</p>
        <form class="tw-mt-2 tw-bg-transparent tw-flex tw-flex-row tw-justify-center">

          <div class="tw-w-3/4 tw-md:w-3/4">
            <input type="email" name="email" id="email" placeholder="Enter your email"
              class="tw-block  tw-bg-gray-300 tw-placeholder-gray-500 tw-w-full  tw-text-black  tw-outline-none  tw-mb-1 tw-p-3"
              required>
          </div>

          <button
            class="tw-group tw-bg-white tw-shadow-lg tw-relative tw-h-12 tw-mb-4 tw-cursor-pointer hover:tw-transform hover:tw-translate-x-2 hover:tw-transition-transform hover:tw-duration-300 tw-w-48 tw-overflow-hidden tw-text-lg">
            <div
              class="tw-absolute tw-inset-0 tw-w-full bg-color tw--transition-all tw-duration-[250ms] tw-ease-out group-hover:tw-w-full">
            </div>
            <span class="tw-relative tw-inline-flex tw-items-center tw-gap-2 tw-text-black group-hover:tw-text-white">
              Subscribe

            </span>
          </button>
        </form>
      </div>


      <div class="tw-relative tw-p-12 tw-pb-4">
        <div class="tw-mx-12 tw-px-8 tw-flex tw-flex-row tw-justify-center">

          <v-row>

            <v-col class="tw-mt-8" cols="12" md="3" lg="3">
              <h3 class="tw-text-white tw-font-extrabold tw-mb-4 tw-uppercase">Support</h3>
              <ul class="tw-list-disc tw-list-inside tw-text-gray-400 tw-leading-6">
                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">Contact us</a>
                </li>

                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">Find a Store</a>
                </li>
                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">FAQ</a>
                </li>


              </ul>
            </v-col>

            <v-col class="tw-mt-8" cols="12" md="3" lg="3">
              <h3 class="tw-text-white tw-font-extrabold tw-mb-4 tw-uppercase">Customers</h3>
              <ul class="tw-list-disc tw-list-inside tw-text-gray-400 tw-leading-6">
                <li>
                  <a href="/privacy" class="tw-text-white tw-text-sm">Free Samples</a>
                </li>
                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">Affiliate</a>
                </li>

                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">Enquiries</a>
                </li>
                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">FAQs</a>
                </li>


              </ul>
            </v-col>
            <v-col class="tw-mt-8" cols="12" md="3" lg="3">
              <h3 class="tw-text-white tw-font-extrabold tw-mb-4">About Us</h3>
              <ul class="tw-list-disc tw-list-inside tw-text-gray-400 tw-leading-6">
                <li>
                  <a href="/privacy" class="tw-text-white tw-text-sm">Our Story</a>
                </li>
                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">Our Blog</a>
                </li>

                <li>
                  <a href="/privacy" class="tw-text-white tw-text-sm">Sitemap</a>
                </li>

                <li>
                  <a href="/privacy" class="tw-text-white tw-text-sm">FAQs</a>
                </li>


              </ul>
            </v-col>


            <v-col class="tw-mt-8" cols="12" md="3" lg="3">
              <h3 class="tw-text-white tw-font-extrabold tw-mb-4">Legal</h3>
              <ul class="tw-list-disc tw-list-inside tw-text-gray-400 tw-leading-6">
                <li>
                  <a href="/privacy" class="tw-text-white tw-text-sm">Sustainability</a>
                </li>
                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">Privacy Policy</a>
                </li>

                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">Terms and Condition</a>
                </li>
                <li>
                  <a href="/contact" class="tw-text-white tw-text-sm">Cookie Policy</a>
                </li>


              </ul>
            </v-col>

          </v-row>
        </div>


        <ul class="tw-flex tw-flex-row lg:tw-justify-center tw-px-20 lg:tw-px-0 tw-mt-8 tw-items-center tw-gap-4">
          <li>
            <a href="#" target="_blank" class="tw-text-white">
              <svg class="tw-bg-white tw-rounded tw-p-1" width="24" height="24" viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg" fill="#000000">
                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                <g id="SVGRepo_iconCarrier">
                  <g>
                    <path fill="none" d="M0 0h24v24H0z"></path>
                    <path
                      d="M14 13.5h2.5l1-4H14v-2c0-1.03 0-2 2-2h1.5V2.14c-.326-.043-1.557-.14-2.857-.14C11.928 2 10 3.657 10 6.7v2.8H7v4h3V22h4v-8.5z">
                    </path>
                  </g>
                </g>
              </svg>
            </a>
          </li>

          <li>
            <a href="#" target="_blank" class="tw-text-white">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                <g id="SVGRepo_iconCarrier">
                  <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M12 18C15.3137 18 18 15.3137 18 12C18 8.68629 15.3137 6 12 6C8.68629 6 6 8.68629 6 12C6 15.3137 8.68629 18 12 18ZM12 16C14.2091 16 16 14.2091 16 12C16 9.79086 14.2091 8 12 8C9.79086 8 8 9.79086 8 12C8 14.2091 9.79086 16 12 16Z"
                    fill="#ffffff"></path>
                  <path
                    d="M18 5C17.4477 5 17 5.44772 17 6C17 6.55228 17.4477 7 18 7C18.5523 7 19 6.55228 19 6C19 5.44772 18.5523 5 18 5Z"
                    fill="#ffffff"></path>
                  <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M1.65396 4.27606C1 5.55953 1 7.23969 1 10.6V13.4C1 16.7603 1 18.4405 1.65396 19.7239C2.2292 20.8529 3.14708 21.7708 4.27606 22.346C5.55953 23 7.23969 23 10.6 23H13.4C16.7603 23 18.4405 23 19.7239 22.346C20.8529 21.7708 21.7708 20.8529 22.346 19.7239C23 18.4405 23 16.7603 23 13.4V10.6C23 7.23969 23 5.55953 22.346 4.27606C21.7708 3.14708 20.8529 2.2292 19.7239 1.65396C18.4405 1 16.7603 1 13.4 1H10.6C7.23969 1 5.55953 1 4.27606 1.65396C3.14708 2.2292 2.2292 3.14708 1.65396 4.27606ZM13.4 3H10.6C8.88684 3 7.72225 3.00156 6.82208 3.0751C5.94524 3.14674 5.49684 3.27659 5.18404 3.43597C4.43139 3.81947 3.81947 4.43139 3.43597 5.18404C3.27659 5.49684 3.14674 5.94524 3.0751 6.82208C3.00156 7.72225 3 8.88684 3 10.6V13.4C3 15.1132 3.00156 16.2777 3.0751 17.1779C3.14674 18.0548 3.27659 18.5032 3.43597 18.816C3.81947 19.5686 4.43139 20.1805 5.18404 20.564C5.49684 20.7234 5.94524 20.8533 6.82208 20.9249C7.72225 20.9984 8.88684 21 10.6 21H13.4C15.1132 21 16.2777 20.9984 17.1779 20.9249C18.0548 20.8533 18.5032 20.7234 18.816 20.564C19.5686 20.1805 20.1805 19.5686 20.564 18.816C20.7234 18.5032 20.8533 18.0548 20.9249 17.1779C20.9984 16.2777 21 15.1132 21 13.4V10.6C21 8.88684 20.9984 7.72225 20.9249 6.82208C20.8533 5.94524 20.7234 5.49684 20.564 5.18404C20.1805 4.43139 19.5686 3.81947 18.816 3.43597C18.5032 3.27659 18.0548 3.14674 17.1779 3.0751C16.2777 3.00156 15.1132 3 13.4 3Z"
                    fill="#ffffff"></path>
                </g>
              </svg> </a>
          </li>

          <li>
            <a href="#" target="_blank" class="tw-text-white">
              <svg class="tw-bg-white tw-rounded-full tw-p-1" width="24" height="24" fill="#000000" version="1.1"
                xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 512 512"
                xml:space="preserve">
                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                <g id="SVGRepo_iconCarrier">
                  <g id="7935ec95c421cee6d86eb22ecd12951c">
                    <path style="display: inline;"
                      d="M220.646,338.475C207.223,408.825,190.842,476.269,142.3,511.5 c-14.996-106.33,21.994-186.188,39.173-270.971c-29.293-49.292,3.518-148.498,65.285-124.059 c76.001,30.066-65.809,183.279,29.38,202.417c99.405,19.974,139.989-172.476,78.359-235.054 C265.434-6.539,95.253,81.775,116.175,211.161c5.09,31.626,37.765,41.22,13.062,84.884c-57.001-12.65-74.005-57.6-71.822-117.533 c3.53-98.108,88.141-166.787,173.024-176.293c107.34-12.014,208.081,39.398,221.991,140.376 c15.67,113.978-48.442,237.412-163.23,228.529C258.085,368.704,245.023,353.283,220.646,338.475z">
                    </path>
                  </g>
                </g>
              </svg>
            </a>
          </li>

          <li>
            <a href="#" class="tw-text-white">
              <svg width="26" height="26" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
                <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
                <g id="SVGRepo_iconCarrier">
                  <path
                    d="M19.83 8.00001C19.83 8.17001 19.83 8.35001 19.83 8.52001C19.8393 10.0302 19.5487 11.5272 18.9751 12.9242C18.4014 14.3212 17.5562 15.5904 16.4883 16.6583C15.4204 17.7262 14.1512 18.5714 12.7542 19.1451C11.3572 19.7187 9.86017 20.0093 8.34999 20C6.15213 20.0064 3.9992 19.3779 2.14999 18.19C2.47999 18.19 2.78999 18.19 3.14999 18.19C4.96345 18.19 6.72433 17.5808 8.14999 16.46C7.30493 16.4524 6.48397 16.1774 5.80489 15.6744C5.12581 15.1714 4.62349 14.4662 4.36999 13.66C4.62464 13.7006 4.88213 13.7207 5.13999 13.72C5.49714 13.7174 5.85281 13.6738 6.19999 13.59C5.2965 13.4056 4.48448 12.9147 3.90135 12.2003C3.31822 11.486 2.99981 10.5921 2.99999 9.67001C3.55908 9.97841 4.18206 10.153 4.81999 10.18C4.25711 9.80767 3.79593 9.30089 3.47815 8.7055C3.16038 8.11011 2.99604 7.44489 2.99999 6.77001C3.00124 6.06749 3.18749 5.37769 3.53999 4.77001C4.55172 6.01766 5.81423 7.03889 7.24575 7.76757C8.67727 8.49625 10.2459 8.91613 11.85 9.00001C11.7865 8.69737 11.753 8.38922 11.75 8.08001C11.7239 7.25689 11.9526 6.44578 12.4047 5.75746C12.8569 5.06913 13.5104 4.53714 14.2762 4.23411C15.0419 3.93109 15.8826 3.87181 16.6833 4.06437C17.484 4.25693 18.2057 4.69195 18.75 5.31001C19.655 5.12822 20.5214 4.78981 21.31 4.31001C21.0088 5.24317 20.3754 6.0332 19.53 6.53001C20.3337 6.44316 21.1194 6.23408 21.86 5.91001C21.3116 6.71097 20.6361 7.41694 19.86 8.00001H19.83Z"
                    fill="#ffffff"></path>
                </g>
              </svg>
            </a>
          </li>


        </ul>




      </div>
    </footer>


  </div>
</template>


<script>
  export default {
    data() {
      return {
        isOpen: false,
        theme: 'theme-light',
        selectedItem: null,
        hidden: true,
        items: [{
            title: 'Click Me1'
          },
          {
            title: 'Click Me2'
          },
          {
            title: 'Click Me3'
          },
          {
            title: 'Click Me4'
          },
        ],
      };
    },


    mounted() {
      // Toggle dropdown on button click
      const dropdownButton = document.getElementById('dropdownButton');
      const dropdownMenu = document.getElementById('dropdown');

      dropdownButton.addEventListener('click', () => {
        dropdownMenu.classList.toggle('hidden');
      });

      // Close dropdown on outside click
      document.addEventListener('click', (event) => {
        if (!dropdownButton.contains(event.target) && !dropdownMenu.contains(event.target)) {
          dropdownMenu.classList.add('hidden');
        }
      });
    },


    methods: {

      toggleMenu() {
        this.isOpen = !this.isOpen;
      },
      closeMenu() {
        this.isOpen = false;
      },
      closeDialog() {
        this.$emit("close");
      },
      openModal() {
        this.modalVisible = true;
      }

    },



  }

</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Josefin+Sans&family=Poppins&display=swap');

  footer {
    background-color: black;
  }

  button {
    border: 0.5px solid #FFF500;
  }

  button:hover {
    border: none;
  }

  .text-color {
    color: #FFF500;
  }

  .bg-color {
    background-color: #FFF500;
  }

  .font-sans {
    font-family: 'Josefin Sans', sans-serif;
    font-family: 'Poppins', sans-serif;
  }

  /* Popup */
  .tw-modal {
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease-in-out;
  }

  .tw-modal-overlay {
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease-in-out;
  }

  .tw-modal-container {
    opacity: 0;
    visibility: hidden;
    transform: translateY(-50px);
    transition: all 0.3s ease-in-out;
  }

  .tw-modal .tw-modal-overlay {
    opacity: 1;
    visibility: visible;
  }

  .tw-modal.open {
    opacity: 1;
    visibility: visible;
  }

  /* Modal backdrop styles */
  .tw-modal-backdrop {
    z-index: 50;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }

  /* Modal content styles */
  .tw-modal {
    background-color: white;
    padding: 2rem;
    border-radius: 0.5rem;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  }

  /* Close button styles */
  .tw-modal-close-btn {
    background-color: gray;
    color: white;
    border: none;
    padding: 0.5rem 1rem;
    border-radius: 0.25rem;
    cursor: pointer;
  }

  /* Button styles */

  /* Popup */
  .tw-modal {
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease-in-out;
  }

  .tw-modal-overlay {
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease-in-out;
  }

  .tw-modal-container {
    opacity: 0;
    visibility: hidden;
    transform: translateY(-50px);
    transition: all 0.3s ease-in-out;
  }

  .tw-modal .tw-modal-overlay {
    opacity: 1;
    visibility: visible;
  }

  .tw-modal.open {
    opacity: 1;
    visibility: visible;
  }

  .tw-modal.open .tw-modal-container {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
  }

  /* Close button */
  .tw-modal-close {
    cursor: pointer;
  }

  /* Animation */
  @keyframes fadeIn {
    from {
      opacity: 0;
    }

    to {
      opacity: 1;
    }
  }

  .animated {
    animation-duration: 0.3s;
    animation-fill-mode: both;
  }

  .fadeIn {
    animation-name: fadeIn;
  }

</style>
