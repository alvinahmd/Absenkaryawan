<template>
  <div class="max-w-screen-sm mx-auto">
    <div class="flex flex-row py-5 px-4 bg-white shadow-lg my-0 mx-auto min-h-full max-w-screen-sm">
      <div class="mx-auto items-center">
        <img src="/manggala.png" class="">
      </div>
      <img src="/lonceng.svg">
    </div>
    <div class="">
      <table class="items-center w-full border">
        <thead>
          <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(242, 251, 255, 1)">
            <th class="py-4 px-4">
              <img src="/sampah2.svg">
            </th>
            <th class="pr-16 text-gray-600">
              7.35 PM
            </th>
            <th class="pr-20 text-gray-600">
              27 Feb 2023
            </th>
            <th class="pr-16 text-gray-600">
              16.54 PM
            </th>
          </tr>
        </thead>
        <thead>
          <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(242, 251, 255, 1)">
            <th class="py-4 px-4">
              <img src="/sampah2.svg">
            </th>
            <th class="pr-16 text-gray-600">
              7.35 PM
            </th>
            <th class="pr-20 text-gray-600">
              28 Feb 2023
            </th>
            <th class="pr-16 text-gray-600">
              16.54 PM
            </th>
          </tr>
        </thead>
        <thead>
          <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(242, 251, 255, 1)">
            <th class="py-4 px-4">
              <img src="/sampah2.svg">
            </th>
            <th class="pr-16 text-gray-600">
              7.35 PM
            </th>
            <th class="pr-20 text-gray-600">
              1 Mar 2023
            </th>
            <th class="pr-16 text-gray-600">
              16.54 PM
            </th>
          </tr>
        </thead>
        <thead>
          <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(242, 251, 255, 1)">
            <th class="py-4 px-4">
              <img src="/sampah2.svg">
            </th>
            <th class="pr-16 text-gray-600">
              7.35 PM
            </th>
            <th class="pr-20 text-gray-600">
              2 Mar 2023
            </th>
            <th class="pr-16 text-gray-600">
              16.54 PM
            </th>
          </tr>
        </thead>
        <thead>
          <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(242, 251, 255, 1)">
            <th class="py-4 px-4">
              <img src="/sampah2.svg">
            </th>
            <th class="pr-16 text-gray-600">
              7.35 PM
            </th>
            <th class="pr-20 text-gray-600">
              3 Mar 2023
            </th>
            <th class="pr-16 text-gray-600">
              16.54 PM
            </th>
          </tr>
        </thead>
        <thead>
          <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(242, 251, 255, 1)">
            <th class="py-4 px-4">
              <img src="/sampah2.svg">
            </th>
            <th class="pr-16 text-gray-600">
              7.35 PM
            </th>
            <th class="pr-20 text-gray-600">
              4 Mar 2023
            </th>
            <th class="pr-16 text-gray-600">
              16.54 PM
            </th>
          </tr>
        </thead>
        <thead>
          <tr class="border-b text-white rounded-t-xl" style="background-color: rgba(242, 251, 255, 1)">
            <th class="py-4 px-4">
              <img src="/sampah2.svg">
            </th>
            <th class="pr-16 text-gray-600">
              7.35 PM
            </th>
            <th class="pr-20 text-gray-600">
              5 Mar 2023
            </th>
            <th class="pr-16 text-gray-600">
              ------
            </th>
          </tr>
        </thead>
      </table>
    </div>
    <div class="my-0 mx-auto min-h-full max-w-screen-sm">
      <div class="container">
        <div class="relative  flex flex-row py-2 px-4 bg-white shadow-lg">
          <div class="flex list-none flex-col flex-wrap border-b-0 pl-0 md:flex-row">
            <a href="/" class="font-medium px-20 mx-auto">
              Check In
            </a>
          </div>
          <a
            href="/"
            class="font-medium px-20 mx-auto"
          >Check out</a>
          <img src="/timer.svg" class="pr-2">
        </div>
        <div class="py-8 px-24">
          <img src="/bulat.svg" class="items-center pl-28 transition hover:ease-in-out transform hover:scale-105">
        </div>
        <div class="my-0 mx-auto min-h-full max-w-screen-sm">
          <div class="container mb-4" />
          <div class="w-full bg-white py-4">
            <div>
              <ul class="flex justify-between px-14 items-center">
                <li>
                  <router-link to="/">
                    <img src="/vector.png" class="pl-2">
                    <div class="text-blue-500 text-center">
                      Home
                    </div>
                  </router-link>
                </li>
                <li class="text-white">
                  <a href="https://meet.google.com/pwg-zcyr-bcp">
                    <img src="/vc1.png" alt="">
                    <span class="text-gray-400 ">Meet</span>
                  </a>
                </li>
                <li>
                  <router-link to="/Tiket">
                    <img src="/chat.png" alt="">
                    <span class="text-gray-400">Chat</span>
                  </router-link>
                </li>
                <li>
                  <router-link to="/proflogin">
                    <img src="/profil.png" class="pl-2">
                    <span class="text-gray-400">Profile</span>
                  </router-link>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      persik: null
    }
  }
}
</script>
