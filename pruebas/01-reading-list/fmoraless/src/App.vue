<script setup>
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'

// initialize components based on data attribute selectors
onMounted(() => {
  initFlowbite()
})
</script>

<template>
  <div class="antialiased bg-gray-50 dark:bg-gray-900">
    <nav
      class="bg-white border-b border-gray-200 px-4 py-2.5 dark:bg-gray-800 dark:border-gray-700 fixed left-0 right-0 top-0 z-50"
    >
      <div class="flex flex-wrap justify-between items-center">
        <div class="flex justify-start items-center">
          <button
            data-drawer-target="drawer-navigation"
            data-drawer-toggle="drawer-navigation"
            aria-controls="drawer-navigation"
            class="p-2 mr-2 text-gray-600 rounded-lg cursor-pointer md:hidden hover:text-gray-900 hover:bg-gray-100 focus:bg-gray-100 dark:focus:bg-gray-700 focus:ring-2 focus:ring-gray-100 dark:focus:ring-gray-700 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white"
          >
            <svg
              aria-hidden="true"
              class="w-6 h-6"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h6a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
                clip-rule="evenodd"
              ></path>
            </svg>
            <svg
              aria-hidden="true"
              class="hidden w-6 h-6"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                clip-rule="evenodd"
              ></path>
            </svg>
            <span class="sr-only">Toggle sidebar</span>
          </button>
          <a href="https://flowbite.com" class="flex items-center justify-between mr-4">
            <img
              src="https://flowbite.s3.amazonaws.com/logo.svg"
              class="mr-3 h-8"
              alt="Flowbite Logo"
            />
            <span class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white"
              >BOOKS</span
            >
          </a>
          <form action="#" method="GET" class="hidden md:block md:pl-2">
            <label for="topbar-search" class="sr-only">Search</label>
            <div class="relative md:w-64 md:w-96">
              <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
                <svg
                  class="w-5 h-5 text-gray-500 dark:text-gray-400"
                  fill="currentColor"
                  viewBox="0 0 20 20"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                    d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
                  ></path>
                </svg>
              </div>
              <input
                type="text"
                name="email"
                id="topbar-search"
                class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full pl-10 p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-primary-500 dark:focus:border-primary-500"
                placeholder="Search"
              />
            </div>
          </form>
        </div>
        <div class="flex items-center lg:order-2">
          <button
            type="button"
            data-drawer-toggle="drawer-navigation"
            aria-controls="drawer-navigation"
            class="p-2 mr-1 text-gray-500 rounded-lg md:hidden hover:text-gray-900 hover:bg-gray-100 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-700 focus:ring-4 focus:ring-gray-300 dark:focus:ring-gray-600"
          >
            <span class="sr-only">Toggle search</span>
            <svg
              aria-hidden="true"
              class="w-6 h-6"
              fill="currentColor"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                clip-rule="evenodd"
                fill-rule="evenodd"
                d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z"
              ></path>
            </svg>
          </button>
          <!-- Notifications -->

          <!-- Dropdown menu -->
          <div
            class="hidden overflow-hidden z-50 my-4 max-w-sm text-base list-none bg-white rounded divide-y divide-gray-100 shadow-lg dark:divide-gray-600 dark:bg-gray-700 rounded-xl"
            id="notification-dropdown"
          ></div>
          <!-- Apps -->

          <!-- Dropdown menu -->

          <button
            type="button"
            class="flex mx-3 text-sm bg-gray-800 rounded-full md:mr-0 focus:ring-4 focus:ring-gray-300 dark:focus:ring-gray-600"
            id="user-menu-button"
            aria-expanded="false"
            data-dropdown-toggle="dropdown"
          >
            <span class="sr-only">Open user menu</span>
            <img
              class="w-8 h-8 rounded-full"
              src="https://flowbite.s3.amazonaws.com/blocks/marketing-ui/avatars/michael-gough.png"
              alt="user photo"
            />
          </button>
          <!-- Dropdown menu -->
          <div
            class="hidden z-50 my-4 w-56 text-base list-none bg-white rounded divide-y divide-gray-100 shadow dark:bg-gray-700 dark:divide-gray-600 rounded-xl"
            id="dropdown"
          >
            <div class="py-3 px-4">
              <span class="block text-sm font-semibold text-gray-900 dark:text-white"
                >Neil Sims</span
              >
              <span class="block text-sm text-gray-900 truncate dark:text-white"
                >name@flowbite.com</span
              >
            </div>
            <ul class="py-1 text-gray-700 dark:text-gray-300" aria-labelledby="dropdown">
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-400 dark:hover:text-white"
                  >My profile</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:text-gray-400 dark:hover:text-white"
                  >Account settings</a
                >
              </li>
            </ul>
            <ul class="py-1 text-gray-700 dark:text-gray-300" aria-labelledby="dropdown">
              <li>
                <a
                  href="#"
                  class="flex items-center py-2 px-4 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                  ><svg
                    class="mr-2 w-5 h-5 text-gray-400"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M3.172 5.172a4 4 0 015.656 0L10 6.343l1.172-1.171a4 4 0 115.656 5.656L10 17.657l-6.828-6.829a4 4 0 010-5.656z"
                      clip-rule="evenodd"
                    ></path>
                  </svg>
                  My likes</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="flex items-center py-2 px-4 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                  ><svg
                    class="mr-2 w-5 h-5 text-gray-400"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M7 3a1 1 0 000 2h6a1 1 0 100-2H7zM4 7a1 1 0 011-1h10a1 1 0 110 2H5a1 1 0 01-1-1zM2 11a2 2 0 012-2h12a2 2 0 012 2v4a2 2 0 01-2 2H4a2 2 0 01-2-2v-4z"
                    ></path>
                  </svg>
                  Collections</a
                >
              </li>
              <li>
                <a
                  href="#"
                  class="flex justify-between items-center py-2 px-4 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                >
                  <span class="flex items-center">
                    <svg
                      aria-hidden="true"
                      class="mr-2 w-5 h-5 text-primary-600 dark:text-primary-500"
                      fill="currentColor"
                      viewBox="0 0 20 20"
                      xmlns="http://www.w3.org/2000/svg"
                    >
                      <path
                        fill-rule="evenodd"
                        d="M12.395 2.553a1 1 0 00-1.45-.385c-.345.23-.614.558-.822.88-.214.33-.403.713-.57 1.116-.334.804-.614 1.768-.84 2.734a31.365 31.365 0 00-.613 3.58 2.64 2.64 0 01-.945-1.067c-.328-.68-.398-1.534-.398-2.654A1 1 0 005.05 6.05 6.981 6.981 0 003 11a7 7 0 1011.95-4.95c-.592-.591-.98-.985-1.348-1.467-.363-.476-.724-1.063-1.207-2.03zM12.12 15.12A3 3 0 017 13s.879.5 2.5.5c0-1 .5-4 1.25-4.5.5 1 .786 1.293 1.371 1.879A2.99 2.99 0 0113 13a2.99 2.99 0 01-.879 2.121z"
                        clip-rule="evenodd"
                      ></path>
                    </svg>
                    Pro version
                  </span>
                  <svg
                    aria-hidden="true"
                    class="w-5 h-5 text-gray-400"
                    fill="currentColor"
                    viewBox="0 0 20 20"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      fill-rule="evenodd"
                      d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                      clip-rule="evenodd"
                    ></path>
                  </svg>
                </a>
              </li>
            </ul>
            <ul class="py-1 text-gray-700 dark:text-gray-300" aria-labelledby="dropdown">
              <li>
                <a
                  href="#"
                  class="block py-2 px-4 text-sm hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white"
                  >Sign out</a
                >
              </li>
            </ul>
          </div>
        </div>
      </div>
    </nav>

    <!-- Sidebar -->

    <aside
      class="fixed top-0 left-0 z-40 w-64 h-screen pt-14 transition-transform -translate-x-full bg-white border-r border-gray-200 md:translate-x-0 dark:bg-gray-800 dark:border-gray-700"
      aria-label="Sidenav"
      id="drawer-navigation"
    >
      <!-- 
      ******* FILTROS *********
     -->
      <div class="pt-5 mx-5">
        <p class="pb-5">Filtrar</p>

        <label
          for="default-range"
          class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
          >Por páginas</label
        >
        <input
          id="default-range"
          type="range"
          value="50"
          class="w-full h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer dark:bg-gray-700"
        />
      </div>
      <div class="pt-5 mx-5">
        <label for="small" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
          >Género</label
        >
        <select
          id="small"
          class="block w-full p-2 mb-6 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
        >
          <option selected>Choose a genre</option>
          <option value="DR">Drama</option>
          <option value="CF">Ciencia ficcion</option>
          <option value="RM">Realismo mágico</option>
          <option value="AA">Auto ayuda</option>
        </select>
      </div>
    </aside>

    <main class="p-4 md:ml-64 h-auto pt-20">
      <h1 class="text-3xl font-bold text-center text-gray-900 dark:text-white pb-5">Library App</h1>
      <div class="flex flex-row justify-center">
        <!-- 
            **************** Books ***************
        -->

        <div class="bg-slate-400 basis-4/6 py-3">
          <h1 class="text-3xl font-bold text-center text-gray-900 dark:text-white pb-5">
            Your Books
          </h1>
          <div class="flex flex-wrap mx-4">
            <!-- Libro 1 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img
                    class="rounded-t-lg"
                    src="https://i0.wp.com/www.marcelopedra.com.ar/blog/wp-content/uploads/2014/01/lrg.jpg?ssl=1"
                    alt=""
                    width="300px"
                    height="40px"
                  />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
            <!-- Libro 2 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img
                    class="rounded-t-lg"
                    src="https://i0.wp.com/www.marcelopedra.com.ar/blog/wp-content/uploads/2014/01/camello-oreilly-perl.jpg?resize=432%2C567&ssl=1"
                    alt=""
                    width="300px"
                    height="40px"
                  />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
            <!-- Libro 3 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img
                    class="rounded-t-lg"
                    src="data:image/jpeg;base64,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"
                    alt=""
                    width="300px"
                    height="400px"
                  />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
            <!-- otra fila -->
            <!-- Libro 1 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img class="rounded-t-lg" src="/docs/images/blog/image-1.jpg" alt="" />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
            <!-- Libro 2 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img class="rounded-t-lg" src="/docs/images/blog/image-1.jpg" alt="" />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
            <!-- Libro 3 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img class="rounded-t-lg" src="/docs/images/blog/image-1.jpg" alt="" />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>

            <!-- otra fila 3 -->
            <!-- Libro 1 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img class="rounded-t-lg" src="/docs/images/blog/image-1.jpg" alt="" />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
            <!-- Libro 2 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img class="rounded-t-lg" src="/docs/images/blog/image-1.jpg" alt="" />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
            <!-- Libro 3 -->
            <div class="w-1/3 px-4 mb-8">
              <div
                class="basis-1/4 max-w-sm bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
              >
                <a href="#">
                  <img class="rounded-t-lg" src="/docs/images/blog/image-1.jpg" alt="" />
                </a>
                <div class="p-5">
                  <a href="#">
                    <h5
                      class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                    >
                      Noteworthy technology acquisitions 2021
                    </h5>
                  </a>
                  <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">
                    Here are the biggest enterprise technology acquisitions of 2021 so far, in
                    reverse chronological order.
                  </p>
                  <a
                    href="#"
                    class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
                  >
                    Read more
                    <svg
                      class="w-3.5 h-3.5 ml-2"
                      aria-hidden="true"
                      xmlns="http://www.w3.org/2000/svg"
                      fill="none"
                      viewBox="0 0 14 10"
                    >
                      <path
                        stroke="currentColor"
                        stroke-linecap="round"
                        stroke-linejoin="round"
                        stroke-width="2"
                        d="M1 5h12m0 0L9 1m4 4L9 9"
                      />
                    </svg>
                  </a>
                </div>
              </div>
            </div>
            <!-- 
            **************** fin Books ***************
            -->
          </div>
        </div>

        <!-- 
            **************** FAVORITOS ***************
          -->
        <div class="bg-red-300 basis-2/6 py-3">
          <h1 class="text-3xl font-bold text-center text-gray-900 dark:text-white pb-5">
            Favorite Books
          </h1>
          <div class="mb-8 flex flex-row justify-around gap-3 mx-3">
            <!-- favorito 1 -->
            <div
              class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
            >
              <svg
                class="w-7 h-7 text-gray-500 dark:text-gray-400 mb-3"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 20 20"
              >
                <path
                  d="M18 5h-.7c.229-.467.349-.98.351-1.5a3.5 3.5 0 0 0-3.5-3.5c-1.717 0-3.215 1.2-4.331 2.481C8.4.842 6.949 0 5.5 0A3.5 3.5 0 0 0 2 3.5c.003.52.123 1.033.351 1.5H2a2 2 0 0 0-2 2v3a1 1 0 0 0 1 1h18a1 1 0 0 0 1-1V7a2 2 0 0 0-2-2ZM8.058 5H5.5a1.5 1.5 0 0 1 0-3c.9 0 2 .754 3.092 2.122-.219.337-.392.635-.534.878Zm6.1 0h-3.742c.933-1.368 2.371-3 3.739-3a1.5 1.5 0 0 1 0 3h.003ZM11 13H9v7h2v-7Zm-4 0H2v5a2 2 0 0 0 2 2h3v-7Zm6 0v7h3a2 2 0 0 0 2-2v-5h-5Z"
                />
              </svg>
              <a href="#">
                <h5
                  class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white"
                >
                  Need a help in Claim?
                </h5>
              </a>
              <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">
                Go to this step by step guideline process on how to certify for your weekly
                benefits:
              </p>
              <a href="#" class="inline-flex items-center text-blue-600 hover:underline">
                See our guideline
                <svg
                  class="w-3 h-3 ml-2.5"
                  aria-hidden="true"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 18 18"
                >
                  <path
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M15 11v4.833A1.166 1.166 0 0 1 13.833 17H2.167A1.167 1.167 0 0 1 1 15.833V4.167A1.166 1.166 0 0 1 2.167 3h4.618m4.447-2H17v5.768M9.111 8.889l7.778-7.778"
                  />
                </svg>
              </a>
            </div>
            <div
              class="max-w-sm p-6 bg-white border border-gray-200 rounded-lg shadow dark:bg-gray-800 dark:border-gray-700"
            >
              <svg
                class="w-7 h-7 text-gray-500 dark:text-gray-400 mb-3"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 20 20"
              >
                <path
                  d="M18 5h-.7c.229-.467.349-.98.351-1.5a3.5 3.5 0 0 0-3.5-3.5c-1.717 0-3.215 1.2-4.331 2.481C8.4.842 6.949 0 5.5 0A3.5 3.5 0 0 0 2 3.5c.003.52.123 1.033.351 1.5H2a2 2 0 0 0-2 2v3a1 1 0 0 0 1 1h18a1 1 0 0 0 1-1V7a2 2 0 0 0-2-2ZM8.058 5H5.5a1.5 1.5 0 0 1 0-3c.9 0 2 .754 3.092 2.122-.219.337-.392.635-.534.878Zm6.1 0h-3.742c.933-1.368 2.371-3 3.739-3a1.5 1.5 0 0 1 0 3h.003ZM11 13H9v7h2v-7Zm-4 0H2v5a2 2 0 0 0 2 2h3v-7Zm6 0v7h3a2 2 0 0 0 2-2v-5h-5Z"
                />
              </svg>
              <a href="#">
                <h5
                  class="mb-2 text-2xl font-semibold tracking-tight text-gray-900 dark:text-white"
                >
                  Need a help in Claim?
                </h5>
              </a>
              <p class="mb-3 font-normal text-gray-500 dark:text-gray-400">
                Go to this step by step guideline process on how to certify for your weekly
                benefits:
              </p>
              <a href="#" class="inline-flex items-center text-blue-600 hover:underline">
                See our guideline
                <svg
                  class="w-3 h-3 ml-2.5"
                  aria-hidden="true"
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 18 18"
                >
                  <path
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M15 11v4.833A1.166 1.166 0 0 1 13.833 17H2.167A1.167 1.167 0 0 1 1 15.833V4.167A1.166 1.166 0 0 1 2.167 3h4.618m4.447-2H17v5.768M9.111 8.889l7.778-7.778"
                  />
                </svg>
              </a>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<style scoped></style>
