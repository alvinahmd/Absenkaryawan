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
            New Group
          </h1>
          <div class="justify-end">
            <button class="text-blue-400 font-semibold text-lg">
              Buat
            </button>
          </div>
        </div>
      </div>
      <div class="px-4 py-4  border-b-8 border-gray-100">
        <div class="flex w-full">
          <div class="bg-slate-100 w-20 h-20 rounded-full">
            <div class="flex justify-center translate-y-6">
              <img src="camera.svg" alt="">
            </div>
          </div>
          <div class="px-8 translate-y-4 w-full">
            <input type="text" placeholder="Nama Group" class=" px-4 border-b-2 w-full border-blue-200 outline-none focus:border-blue-400 transition-alls placeholder:font-medium placeholder:text-gray-300 placeholder:text-base">
          </div>
        </div>
      </div>
      <div class="pl-4 py-4">
        <div class="">
          <div class="w-full">
            <p class="font-semibold text-base pb-4" style="color: rgba(68, 68, 68, 1)">
              Add Friends
            </p>
            <div class="px-8">
              <input type="search" placeholder="Cari" class="border-blue-200 rounded-lg h-9 pl-8 pr-2 border-2 w-full transition-all outline-none focus:border-blue-400">
              <div class="-translate-y-6 px-2 ">
                <img src="cari.svg" alt="">
              </div>
            </div>
            <div class="pt-2 pl-4">
              <div class="flex w-full">
                <div class="px-4">
                  <div class=" text-center border w-12 h-12 rounded-full">
                    <p class="text-2xl translate-y-1">
                      L
                    </p>
                  </div>
                </div>
                <div class="flex flex-col border-b w-full">
                  <div class="flex">
                    <h1 class="text-base font-semibold" style="color: rgba(68, 68, 68, 1);">
                      Alvinn
                    </h1>
                  </div>
                  <h1 class="text-xs font-normal w-96" style="color: rgba(68, 68, 68, 1);">
                    Diaz suka ekaa
                  </h1>
                  <div class="flex justify-end -translate-x-8 -translate-y-8">
                    <input id="default-checkbox" type="checkbox" class="w-4 h-4 rounded-full text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500">
                  </div>
                </div>
              </div>
            </div>
            <div class="pt-2 pl-4">
              <div class="flex w-full">
                <div class="px-4">
                  <div class=" text-center border w-12 h-12 rounded-full">
                    <p class="text-2xl translate-y-1">
                      O
                    </p>
                  </div>
                </div>
                <div class="flex flex-col border-b w-full">
                  <div class="flex">
                    <h1 class="text-base font-semibold" style="color: rgba(68, 68, 68, 1);">
                      Diaz
                    </h1>
                  </div>
                  <h1 class="text-xs font-normal w-96" style="color: rgba(68, 68, 68, 1);">
                    Ora yooo hoax
                  </h1>
                  <div class="flex justify-end -translate-x-8 -translate-y-8">
                    <input id="default-checkbox" type="checkbox" class="w-4 h-4 rounded-full text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500">
                  </div>
                </div>
              </div>
            </div>
            <div class="pt-2 pl-4">
              <div class="flex w-full">
                <div class="px-4">
                  <div class=" text-center border w-12 h-12 rounded-full">
                    <p class="text-2xl translate-y-1">
                      V
                    </p>
                  </div>
                </div>
                <div class="flex flex-col border-b w-full">
                  <div class="flex">
                    <h1 class="text-base font-semibold" style="color: rgba(68, 68, 68, 1);">
                      Alvinn
                    </h1>
                  </div>
                  <h1 class="text-xs font-normal w-96" style="color: rgba(68, 68, 68, 1);">
                    Bohongg kamu Kemarin habis cium eka yaaa
                  </h1>
                  <div class="flex justify-end -translate-x-8 -translate-y-8">
                    <input id="default-checkbox" type="checkbox" class="w-4 h-4 rounded-full text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500">
                  </div>
                </div>
              </div>
            </div>
            <div class="pt-2 pl-4">
              <div class="flex w-full">
                <div class="px-4">
                  <div class=" text-center border w-12 h-12 rounded-full">
                    <p class="text-2xl translate-y-1">
                      E
                    </p>
                  </div>
                </div>
                <div class="flex flex-col border-b w-full">
                  <div class="flex">
                    <h1 class="text-base font-semibold" style="color: rgba(68, 68, 68, 1);">
                      Diaz
                    </h1>
                  </div>
                  <h1 class="text-xs font-normal w-96" style="color: rgba(68, 68, 68, 1);">
                    Apaan Ngak yaa Jangan Hoax dong aku masih normal
                  </h1>
                  <div class="flex justify-end -translate-x-8 -translate-y-8">
                    <input id="default-checkbox" type="checkbox" class="w-4 h-4 rounded-full text-blue-600 bg-gray-100 border-gray-300 focus:ring-blue-500">
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
