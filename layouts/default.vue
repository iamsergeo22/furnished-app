<template>
  <div class="font-sans tw-flex tw-flex-col tw-opacity-90">


    <header class="tw-top-0 tw-left-0 tw-right-0 tw-bg-transparent tw-z-50">
      <nav
        class="tw-bg-transparent tw-px-4 lg:tw-px-8 lg:tw-mx-4 tw-pt-8 tw-pb-0 tw-flex tw-flex-row tw-justify-between tw-items-center">

        <div>
          <nuxt-link to="/">
            <h1 class="lg:tw-text-4xl tw-text-xl tw-font-extrabold tw-text-black">
              BLOOMWOODINTERIORS
            </h1>
          </nuxt-link>
        </div>

        <div class="tw-flex lg:tw-gap-4 tw-gap-1 tw-items-center">
          <img class="tw-w-5 tw-h-5" src="../assets/Group.svg" alt="">
          <img class="tw-w-5 tw-h-5" src="../assets/Vector.svg" alt="">
        </div>


      </nav>

      <div class="tw-block lg:tw-hidden tw-px-4 tw-mt-4 tw-flex tw-justify-end tw-mb-4">
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
            <nuxt-link to="#" :class="$route.path === '#' ? 'active' : ''"
              class="text-black font-medium	hover:text-blue-800 text-md hover:no-underline">Contact Us</nuxt-link>
          </li>





        </ul>

        <div
          class="tw-hidden lg:tw-block tw-bg-white tw-items-center lg:tw-justify-between lg:tw-w-1/4 lg:tw-flex tw-rounded-full tw-p-3"
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

      <nav class="bg-color tw-hidden lg:tw-block tw-flex tw-flex-row  tw-px-8 tw-gap-8 tw-py-2 tw-items-center">

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
        <h1 class="tw-text-xl lg:tw-text-4xl tw-font-extrabold tw-text-white tw-mt-8 tw-text-center">
          BLOOMWOODINTERIORS
        </h1>
        <p class="tw-text-md lg:tw-text-xl tw-font-medium tw-text-white tw-text-center">Sign up for exclusive Product
          Offers and Sale Dates</p>
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


      <div class="tw-relative tw-p-8 tw-pb-4">
        <div class="lg:tw-mx-12 lg:tw-px-8 tw-flex tw-flex-row tw-justify-center">

          <v-row>

            <v-col class="tw-mt-8" cols="6" md="3" lg="3">
              <h3 class="tw-text-white tw-font-extrabold tw-mb-4 tw-uppercase">Support</h3>
              <ul class=" tw-text-gray-400 tw-leading-6">
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Contact us</a>
                </li>

                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Find a Store</a>
                </li>
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">FAQ</a>
                </li>


              </ul>
            </v-col>

            <v-col class="tw-mt-8" cols="6" md="3" lg="3">
              <h3 class="tw-text-white tw-font-extrabold tw-mb-4 tw-uppercase">Customers</h3>
              <ul class=" tw-text-gray-400 tw-leading-6">
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Free Samples</a>
                </li>
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Affiliate</a>
                </li>

                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Enquiries</a>
                </li>
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">FAQs</a>
                </li>


              </ul>
            </v-col>
            <v-col class="tw-mt-8" cols="6" md="3" lg="3">
              <h3 class="tw-text-white tw-font-extrabold tw-mb-4">About Us</h3>
              <ul class=" tw-text-gray-400 tw-leading-6">
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Our Story</a>
                </li>
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Our Blog</a>
                </li>

                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Sitemap</a>
                </li>

                <li>
                  <a href="#" class="tw-text-white tw-text-sm">FAQs</a>
                </li>


              </ul>
            </v-col>


            <v-col class="tw-mt-8" cols="6" md="3" lg="3">
              <h3 class="tw-text-white tw-font-extrabold tw-mb-4">Legal</h3>
              <ul class=" tw-text-gray-400 tw-leading-6">
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Sustainability</a>
                </li>
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Privacy Policy</a>
                </li>

                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Terms & Condition</a>
                </li>
                <li>
                  <a href="#" class="tw-text-white tw-text-sm">Cookie Policy</a>
                </li>


              </ul>
            </v-col>

          </v-row>
        </div>


        <ul class="tw-flex tw-flex-row lg:tw-justify-left lg:tw-px-0 tw-mt-8 tw-gap-4">
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

        <div class="tw-mt-4 tw-flex tw-flex-row lg:tw-justify-left lg:tw-px-0 tw-gap-2">

          <a href="#">
            <svg class="tw-bg-white tw-rounded tw-p-1" width="50" height="26" viewBox="0 0 141.732 141.732" xmlns="http://www.w3.org/2000/svg" fill="#000000">
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
              <g id="SVGRepo_iconCarrier">
                <g fill="#2566af">
                  <path
                    d="M62.935 89.571h-9.733l6.083-37.384h9.734zM45.014 52.187L35.735 77.9l-1.098-5.537.001.002-3.275-16.812s-.396-3.366-4.617-3.366h-15.34l-.18.633s4.691.976 10.181 4.273l8.456 32.479h10.141l15.485-37.385H45.014zM121.569 89.571h8.937l-7.792-37.385h-7.824c-3.613 0-4.493 2.786-4.493 2.786L95.881 89.571h10.146l2.029-5.553h12.373l1.14 5.553zm-10.71-13.224l5.114-13.99 2.877 13.99h-7.991zM96.642 61.177l1.389-8.028s-4.286-1.63-8.754-1.63c-4.83 0-16.3 2.111-16.3 12.376 0 9.658 13.462 9.778 13.462 14.851s-12.075 4.164-16.06.965l-1.447 8.394s4.346 2.111 10.986 2.111c6.642 0 16.662-3.439 16.662-12.799 0-9.72-13.583-10.625-13.583-14.851.001-4.227 9.48-3.684 13.645-1.389z">
                  </path>
                </g>
                <path
                  d="M34.638 72.364l-3.275-16.812s-.396-3.366-4.617-3.366h-15.34l-.18.633s7.373 1.528 14.445 7.253c6.762 5.472 8.967 12.292 8.967 12.292z"
                  fill="#e6a540"></path>
                <path fill="none" d="M0 0h141.732v141.732H0z"></path>
              </g>
            </svg>
          </a>

          <a href="#">
            <svg class="tw-bg-white tw-rounded tw-p-1" width="50" height="26" version="1.1" id="Layer_1"
              xmlns:sketch="http://www.bohemiancoding.com/sketch/ns" xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 750 471" enable-background="new 0 0 750 471"
              xml:space="preserve" fill="#000000">
              <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
              <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
              <g id="SVGRepo_iconCarrier">
                <title>Slice 1</title>
                <desc>Created with Sketch.</desc>
                <g id="Page-1" sketch:type="MSPage">
                  <g id="mastercard" sketch:type="MSLayerGroup">
                    <path id="Fill-1" sketch:type="MSShapeGroup" fill="#D9222A"
                      d="M434.008,235.5c0,99.142-80.371,179.504-179.508,179.504 C155.363,415.004,75,334.642,75,235.5c0-99.133,80.362-179.504,179.5-179.504C353.637,55.996,434.008,136.367,434.008,235.5">
                    </path>
                    <path id="Fill-2" sketch:type="MSShapeGroup" fill="#EE9F2D"
                      d="M495.491,55.996c-46.379,0-88.642,17.596-120.5,46.467 c-6.487,5.883-12.546,12.238-18.125,18.996h36.267c4.958,6.029,9.525,12.371,13.684,19.012h-63.634 c-3.813,6.104-7.274,12.446-10.342,19.008h84.313c2.88,6.159,5.421,12.496,7.601,19.004h-99.513 c-2.075,6.191-3.821,12.529-5.217,19.008h109.941c2.638,12.25,4.042,24.967,4.042,38.008c0,19.934-3.254,39.112-9.254,57.021 h-99.513c2.175,6.512,4.717,12.854,7.596,19.008h84.316c-3.074,6.563-6.528,12.904-10.346,19.012h-63.625 c4.154,6.63,8.729,12.98,13.684,18.996h36.259c-5.571,6.771-11.634,13.134-18.13,19.013 c31.858,28.866,74.117,46.454,120.496,46.454C594.629,415.004,675,334.642,675,235.5C675,136.371,594.629,55.996,495.491,55.996">
                    </path>
                    <path id="Fill-3" sketch:type="MSShapeGroup"
                      d="M651.074,335.559c0-3.2,2.592-5.801,5.796-5.801s5.796,2.601,5.796,5.801 c0,3.199-2.592,5.8-5.796,5.8S651.074,338.758,651.074,335.559L651.074,335.559L651.074,335.559z M656.87,339.967 c2.434,0,4.408-1.975,4.408-4.408c0-2.438-1.975-4.404-4.408-4.404c-2.438,0-4.404,1.967-4.404,4.404 C652.466,337.992,654.433,339.967,656.87,339.967L656.87,339.967L656.87,339.967z M656.087,338.108H654.9v-5.096h2.15 c0.45,0,0.908,0,1.304,0.254c0.413,0.279,0.646,0.771,0.646,1.279c0,0.571-0.338,1.104-0.884,1.313l0.938,2.25h-1.316 l-0.779-2.017h-0.871V338.108L656.087,338.108z M656.087,335.217h0.658c0.246,0,0.505,0.021,0.726-0.1 c0.195-0.125,0.296-0.359,0.296-0.584c0-0.195-0.121-0.421-0.288-0.517c-0.208-0.129-0.537-0.101-0.758-0.101h-0.634V335.217 L656.087,335.217z">
                    </path>
                    <path id="Fill-4" sketch:type="MSShapeGroup"
                      d="M212.587,255.154c-2.046-0.238-2.945-0.301-4.35-0.301 c-11.046,0-16.638,3.788-16.638,11.268c0,4.612,2.729,7.545,6.987,7.545C206.525,273.666,212.245,266.108,212.587,255.154 L212.587,255.154L212.587,255.154z M226.758,288.15h-16.146l0.371-7.676c-4.926,6.066-11.496,8.95-20.426,8.95 c-10.563,0-17.804-8.25-17.804-20.229c0-18.024,12.596-28.541,34.217-28.541c2.208,0,5.042,0.199,7.941,0.57 c0.604-2.441,0.763-3.487,0.763-4.8c0-4.908-3.396-6.737-12.5-6.737c-9.533-0.108-17.396,2.271-20.625,3.333 c0.204-1.229,2.7-16.659,2.7-16.659c9.712-2.846,16.116-3.917,23.325-3.917c16.732,0,25.596,7.513,25.579,21.712 c0.033,3.805-0.597,8.5-1.579,14.671C230.883,259.559,227.254,282.546,226.758,288.15L226.758,288.15L226.758,288.15z">
                    </path>
                    <path id="Fill-5" sketch:type="MSShapeGroup"
                      d="M164.6,288.15h-19.487l11.162-69.996L131.35,288.15h-13.279l-1.642-69.596 l-11.733,69.596H86.454l15.237-91.055h28.021l1.7,50.967l17.092-50.967h31.167L164.6,288.15">
                    </path>
                    <path id="Fill-6" sketch:type="MSShapeGroup"
                      d="M519.574,255.154c-2.037-0.238-2.941-0.301-4.342-0.301 c-11.041,0-16.633,3.788-16.633,11.268c0,4.612,2.725,7.545,6.983,7.545C513.521,273.666,519.245,266.108,519.574,255.154 L519.574,255.154L519.574,255.154z M533.758,288.15h-16.146l0.366-7.676c-4.925,6.066-11.5,8.95-20.421,8.95 c-10.566,0-17.8-8.25-17.8-20.229c0-18.024,12.588-28.541,34.213-28.541c2.208,0,5.037,0.199,7.933,0.57 c0.604-2.441,0.763-3.487,0.763-4.8c0-4.908-3.392-6.737-12.496-6.737c-9.533-0.108-17.387,2.271-20.629,3.333 c0.204-1.229,2.709-16.659,2.709-16.659c9.712-2.846,16.112-3.917,23.313-3.917c16.741,0,25.604,7.513,25.587,21.712 c0.033,3.805-0.596,8.5-1.579,14.671C537.887,259.559,534.25,282.546,533.758,288.15L533.758,288.15L533.758,288.15z">
                    </path>
                    <path id="Fill-7" sketch:type="MSShapeGroup"
                      d="M313.366,287.025c-5.333,1.679-9.491,2.399-14,2.399 c-9.962,0-15.399-5.725-15.399-16.267c-0.142-3.271,1.433-11.879,2.671-19.737c1.125-6.917,8.449-50.529,8.449-50.529h19.371 l-2.263,11.208h11.7l-2.642,17.796h-11.742c-2.25,14.083-5.454,31.625-5.491,33.95c0,3.816,2.037,5.483,6.671,5.483 c2.221,0,3.941-0.226,5.254-0.7L313.366,287.025">
                    </path>
                    <path id="Fill-8" sketch:type="MSShapeGroup"
                      d="M372.758,286.425c-6.654,2.034-13.075,3.017-19.879,3 c-21.684-0.021-32.987-11.346-32.987-33.033c0-25.313,14.379-43.946,33.899-43.946c15.971,0,26.171,10.433,26.171,26.796 c0,5.429-0.7,10.729-2.388,18.212H339c-1.305,10.741,5.57,15.217,16.837,15.217c6.934,0,13.188-1.429,20.142-4.663 L372.758,286.425L372.758,286.425z M361.87,242.525c0.108-1.542,2.055-13.217-9.013-13.217c-6.17,0-10.583,4.704-12.379,13.217 H361.87L361.87,242.525z">
                    </path>
                    <path id="Fill-9" sketch:type="MSShapeGroup"
                      d="M238.446,237.508c0,9.367,4.542,15.826,14.842,20.676 c7.892,3.708,9.112,4.809,9.112,8.17c0,4.617-3.479,6.701-11.191,6.701c-5.813,0-11.221-0.908-17.458-2.922 c0,0-2.563,16.321-2.68,17.101c4.43,0.967,8.38,1.862,20.279,2.191c20.563,0,30.059-7.829,30.059-24.75 c0-10.175-3.976-16.146-13.737-20.634c-8.171-3.75-9.108-4.587-9.108-8.045c0-4.004,3.237-6.046,9.537-6.046 c3.825,0,9.05,0.408,14,1.112l2.775-17.175c-5.046-0.8-12.696-1.442-17.15-1.442C245.925,212.446,238.379,223.833,238.446,237.508 ">
                    </path>
                    <path id="Fill-10" sketch:type="MSShapeGroup"
                      d="M467.533,214.392c5.412,0,10.458,1.421,17.412,4.921l3.188-19.763 c-2.854-1.121-12.904-7.7-21.417-7.7c-13.041,0-24.066,6.471-31.82,17.15c-11.309-3.746-15.958,3.825-21.658,11.367l-5.063,1.179 c0.383-2.483,0.729-4.95,0.612-7.446h-17.896c-2.446,22.917-6.779,46.128-10.171,69.075l-0.884,4.976h19.496 c3.254-21.143,5.037-34.68,6.121-43.842l7.341-4.084c1.097-4.078,4.529-5.458,11.417-5.291c-0.899,4.833-1.383,9.916-1.383,15.184 c0,24.225,13.07,39.308,34.05,39.308c5.404,0,10.041-0.712,17.221-2.658l3.429-20.759c-6.458,3.18-11.758,4.676-16.558,4.676 c-11.329,0-18.184-8.363-18.184-22.184C442.787,228.45,452.983,214.392,467.533,214.392">
                    </path>
                    <path id="Fill-12" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M170.208,282.742h-19.491l11.171-69.988l-24.926,69.988h-13.283 l-1.642-69.588l-11.733,69.588H92.063L107.3,191.7h28.021l0.788,56.362l18.904-56.362h30.267L170.208,282.742">
                    </path>
                    <path id="Fill-11" sketch:type="MSShapeGroup"
                      d="M632.521,197.096l-4.321,26.309c-5.329-7.013-11.054-12.088-18.612-12.088 c-9.833,0-18.783,7.455-24.642,18.425c-8.158-1.692-16.596-4.563-16.596-4.563l-0.004,0.067c0.658-6.134,0.921-9.875,0.862-11.146 h-17.9c-2.438,22.917-6.771,46.128-10.158,69.075l-0.892,4.976h19.492c2.633-17.096,4.649-31.292,6.133-42.551 c6.658-6.016,9.992-11.266,16.721-10.916c-2.979,7.204-4.725,15.504-4.725,24.017c0,18.513,9.366,30.725,23.533,30.725 c7.142,0,12.621-2.462,17.967-8.171l-0.913,6.884H636.9l14.842-91.042H632.521L632.521,197.096z M608.15,271.037 c-6.633,0-9.983-4.908-9.983-14.596c0-14.554,6.271-24.875,15.112-24.875c6.696,0,10.321,5.104,10.321,14.509 C623.6,260.754,617.229,271.037,608.15,271.037L608.15,271.037L608.15,271.037z">
                    </path>
                    <path id="Fill-13" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M218.192,249.758c-2.042-0.236-2.946-0.299-4.346-0.299 c-11.046,0-16.634,3.787-16.634,11.266c0,4.604,2.729,7.547,6.979,7.547C212.138,268.271,217.859,260.713,218.192,249.758 L218.192,249.758L218.192,249.758z M232.37,282.742h-16.146l0.367-7.663c-4.921,6.054-11.5,8.95-20.421,8.95 c-10.567,0-17.805-8.25-17.805-20.229c0-18.033,12.592-28.542,34.217-28.542c2.208,0,5.042,0.2,7.938,0.571 c0.604-2.441,0.763-3.487,0.763-4.808c0-4.909-3.392-6.729-12.496-6.729c-9.537-0.108-17.396,2.271-20.629,3.321 c0.204-1.225,2.7-16.637,2.7-16.637c9.708-2.858,16.12-3.929,23.32-3.929c16.737,0,25.604,7.517,25.588,21.704 c0.029,3.821-0.604,8.513-1.584,14.675C236.495,254.15,232.863,277.15,232.37,282.742L232.37,282.742L232.37,282.742z">
                    </path>
                    <path id="Fill-14" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M493.745,194.15l-3.191,19.767c-6.95-3.496-12-4.92-17.408-4.92 c-14.55,0-24.75,14.058-24.75,34.107c0,13.821,6.858,22.18,18.184,22.18c4.8,0,10.096-1.492,16.554-4.675l-3.421,20.75 c-7.184,1.958-11.816,2.671-17.225,2.671c-20.976,0-34.05-15.084-34.05-39.309c0-32.55,18.058-55.3,43.887-55.3 C480.833,189.421,490.887,193.029,493.745,194.15">
                    </path>
                    <path id="Fill-15" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M525.188,249.758c-2.042-0.236-2.942-0.299-4.347-0.299 c-11.041,0-16.633,3.787-16.633,11.266c0,4.604,2.729,7.547,6.983,7.547C519.129,268.271,524.854,260.713,525.188,249.758 L525.188,249.758L525.188,249.758z M539.366,282.742h-16.15l0.371-7.663c-4.925,6.054-11.5,8.95-20.421,8.95 c-10.563,0-17.804-8.25-17.804-20.229c0-18.033,12.596-28.542,34.212-28.542c2.213,0,5.042,0.2,7.942,0.571 c0.6-2.441,0.762-3.487,0.762-4.808c0-4.909-3.392-6.729-12.495-6.729c-9.533-0.108-17.396,2.271-20.63,3.321 c0.204-1.225,2.704-16.637,2.704-16.637c9.709-2.858,16.117-3.929,23.317-3.929c16.741,0,25.604,7.517,25.583,21.704 c0.033,3.821-0.596,8.513-1.579,14.675C543.495,254.15,539.854,277.15,539.366,282.742L539.366,282.742L539.366,282.742z">
                    </path>
                    <path id="Fill-16" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M318.975,281.621c-5.338,1.679-9.496,2.408-14,2.408 c-9.962,0-15.399-5.725-15.399-16.267c-0.138-3.279,1.438-11.88,2.675-19.737c1.12-6.926,8.445-50.534,8.445-50.534h19.367 l-2.259,11.212h9.941l-2.646,17.788h-9.975c-2.25,14.092-5.463,31.621-5.496,33.95c0,3.83,2.041,5.483,6.671,5.483 c2.221,0,3.938-0.216,5.254-0.691L318.975,281.621">
                    </path>
                    <path id="Fill-17" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M378.366,281.029c-6.65,2.033-13.079,3.012-19.879,3 c-21.684-0.021-32.987-11.346-32.987-33.033c0-25.321,14.379-43.95,33.899-43.95c15.971,0,26.171,10.429,26.171,26.8 c0,5.434-0.7,10.733-2.383,18.213h-38.575c-1.305,10.741,5.57,15.221,16.837,15.221c6.93,0,13.188-1.434,20.138-4.676 L378.366,281.029L378.366,281.029z M367.475,237.117c0.116-1.538,2.059-13.217-9.013-13.217c-6.167,0-10.579,4.717-12.375,13.217 H367.475L367.475,237.117z">
                    </path>
                    <path id="Fill-18" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M244.054,232.112c0,9.366,4.542,15.817,14.842,20.675 c7.892,3.709,9.112,4.813,9.112,8.172c0,4.616-3.483,6.699-11.188,6.699c-5.816,0-11.225-0.908-17.467-2.921 c0,0-2.554,16.321-2.671,17.101c4.421,0.967,8.375,1.85,20.275,2.191c20.566,0,30.059-7.829,30.059-24.746 c0-10.18-3.971-16.15-13.737-20.637c-8.167-3.759-9.113-4.584-9.113-8.046c0-4,3.246-6.059,9.542-6.059 c3.821,0,9.046,0.421,14.004,1.125l2.771-17.179c-5.042-0.8-12.692-1.441-17.146-1.441 C251.533,207.046,243.991,218.425,244.054,232.112">
                    </path>
                    <path id="Fill-19" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M642.508,282.742h-18.438l0.917-6.893 c-5.346,5.717-10.825,8.18-17.967,8.18c-14.167,0-23.529-12.213-23.529-30.725c0-24.63,14.521-45.392,31.708-45.392 c7.559,0,13.279,3.087,18.604,10.096l4.325-26.308h19.221L642.508,282.742L642.508,282.742z M613.762,265.633 c9.075,0,15.45-10.283,15.45-24.953c0-9.405-3.629-14.509-10.325-14.509c-8.837,0-15.116,10.316-15.116,24.875 C603.771,260.733,607.129,265.633,613.762,265.633L613.762,265.633L613.762,265.633z">
                    </path>
                    <path id="Fill-20" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M556.92,208.704c-2.441,22.917-6.774,46.13-10.162,69.063 l-0.892,4.976h19.491c6.972-45.275,8.659-54.117,19.588-53.009c1.742-9.267,4.983-17.383,7.4-21.479 c-8.163-1.7-12.721,2.913-18.688,11.675c0.471-3.788,1.333-7.467,1.162-11.225H556.92">
                    </path>
                    <path id="Fill-21" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M396.5,208.704c-2.446,22.917-6.779,46.13-10.167,69.063 l-0.888,4.976h19.5c6.963-45.275,8.646-54.117,19.571-53.009c1.75-9.267,4.991-17.383,7.399-21.479 c-8.154-1.7-12.717,2.913-18.679,11.675c0.471-3.788,1.325-7.467,1.162-11.225H396.5">
                    </path>
                    <path id="Fill-22" sketch:type="MSShapeGroup" fill="#FFFFFF"
                      d="M651.067,276.945c0-3.212,2.596-5.799,5.796-5.799 c3.204,0,5.796,2.587,5.796,5.799c0,3.196-2.592,5.797-5.796,5.797C653.662,282.742,651.067,280.142,651.067,276.945 L651.067,276.945L651.067,276.945z M656.863,281.35c2.438,0,4.404-1.975,4.404-4.404c0-2.433-1.967-4.408-4.404-4.408 c-2.434,0-4.408,1.976-4.408,4.408C652.454,279.375,654.429,281.35,656.863,281.35L656.863,281.35L656.863,281.35z M656.079,279.479h-1.188v-5.082h2.153c0.446,0,0.909,0.008,1.296,0.254c0.417,0.283,0.654,0.766,0.654,1.274 c0,0.575-0.337,1.112-0.888,1.317l0.942,2.236h-1.321l-0.779-2.008h-0.87V279.479L656.079,279.479z M656.079,276.6h0.653 c0.246,0,0.513,0.018,0.729-0.1c0.196-0.125,0.296-0.362,0.296-0.588c0-0.188-0.116-0.412-0.287-0.524 c-0.204-0.116-0.542-0.083-0.763-0.083h-0.629V276.6L656.079,276.6z">
                    </path>
                  </g>
                </g>
              </g>
            </svg> </a>



        </div>




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
