<template>
  <div>
    <div class="max-w-xl w-full mx-auto bg-white shadow-lg h-screen">
      <div class="py-5 px-4  border-b-2">
        <div class="flex">
          <a href="/chat">
            <svg width="11" height="19" viewBox="0 0 11 19" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M9 2L3 9.1875L9 17" stroke="#0075FF" stroke-width="4" stroke-linecap="round" />
            </svg>
          </a>
          <h1 class="font-medium text-base mx-auto pl-4" style="color:rgba(50, 11, 78, 1)">
            Add Friends
          </h1>
          <div class="justify-end">
            <div class="border-2 w-14 rounded-full border-blue-400">
              <div class="flex px-2">
                <img src="human.svg" alt="">
                <p class=" pl-2 font-semibold text-base text-center" style="color: rgba(68, 68, 68, 1)">
                  0
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="px-4 py-4">
        <div class="w-full">
          <div class="flex flex-col w-full">
            <input type="text" placeholder="ID 123456" class=" px-4 w-full h-14 bg-gray-200 rounded-lg placeholder:text-gray-300 placeholder:font-medium focus:ring-2 focus:ring-blue-300 focus:outline-none transition-all focus:transition-all">
            <p class="text-xs font-semibold text-gray-300">
              ID mu adalah 123456
            </p>
          </div>
        </div>
        <div class="py-4">
          <div class="w-full">
            <button class="w-full bg-blue-500 hover:opacity-80 transition-all rounded-lg py-2 text-white font-semibold text-base focus:placeholder-opacity-100 focus:ring focus:ring-blue-600">
              Kirim Permintaan Pertemanan
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
