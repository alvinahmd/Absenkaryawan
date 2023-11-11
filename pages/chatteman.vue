<template>
  <div>
    <div class="max-w-xl w-full mx-auto bg-white shadow-lg h-full">
      <div class="py-5 px-4  border-b-2">
        <div class="flex">
          <a href="/chat" class="translate-y-2">
            <svg width="11" height="19" viewBox="0 0 11 19" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M9 2L3 9.1875L9 17" stroke="#0075FF" stroke-width="4" stroke-linecap="round" />
            </svg>
          </a>
          <div class="flex mx-auto ">
            <div class="border w-10 h-10 rounded-full">
              <div class="text-center text-sm font-medium translate-y-2" style="color: rgba(68, 68, 68, 1);">
                p
              </div>
            </div>
            <h1 class="text-base font-medium pl-4 text-center translate-y-2" style="color: rgba(68, 68, 68, 1);">
              Alvin
            </h1>
          </div>
          <div class="justify-end translate-y-2">
            <img src="vc.svg" alt="">
          </div>
        </div>
      </div>
      <div class="px-12 py-4">
        <div class="relative">
          <div class="pb-2">
            <div class=" w-max h-12 rounded-lg" style="background-color:rgba(46, 182, 255, 1)">
              <p class="text-white py-2 px-2 text-xs font-sans font-medium">
                Hallo aku Diaz
              </p>
            </div>
          </div>
          <div class="pb-2">
            <div class=" w-max h-12 rounded-lg" style="background-color:rgba(46, 182, 255, 1)">
              <p class="text-white py-2 px-2 text-xs font-sans font-medium">
                Kamu apa temenya eka nur yaa
              </p>
            </div>
          </div>
          <div class="pb-2">
            <div class=" w-max h-12 rounded-lg" style="background-color:rgba(46, 182, 255, 1)">
              <p class="text-white py-2 px-2 text-xs font-sans font-medium">
                Aku suka sama ekaa tolong bantuin aku dong
              </p>
            </div>
          </div>
          <div class="pb-2">
            <div class=" w-max h-12 rounded-lg" style="background-color:rgba(46, 182, 255, 1)">
              <p class="text-white py-2 px-2 text-xs font-sans font-medium">
                bantuuinn deketin aku sama ekaa
              </p>
            </div>
          </div>
        </div>
        <div class="pl-4 flex justify-end">
          <div class="flex flex-col">
            <div class="pb-2">
              <div class=" w-max h-12 rounded-lg" style="background-color:rgba(46, 182, 255, 1)">
                <p class="text-white py-2 px-2 text-xs font-sans font-medium">
                  iya kenapaa
                </p>
              </div>
            </div>
            <div class="pb-2">
              <div class=" w-max h-12 rounded-lg" style="background-color:rgba(46, 182, 255, 1)">
                <p class="text-white py-2 px-2 text-xs font-sans font-medium">
                  iya aku temennya ekaa ada apaa
                </p>
              </div>
            </div>
            <div class="pb-2">
              <div class=" w-max h-12 rounded-lg" style="background-color:rgba(46, 182, 255, 1)">
                <p class="text-white py-2 px-2 text-xs font-sans font-medium">
                  Bantuin gimana yaaa
                </p>
              </div>
            </div>
            <div class="pb-2">
              <div class=" w-max h-12 rounded-lg" style="background-color:rgba(46, 182, 255, 1)">
                <p class="text-white py-2 px-2 text-xs font-sans font-medium">
                  eummm gimanaaa yaa
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="my-0 mx-auto max-w-xl" style="box-shadow: 0px -2px 4px 0px rgba(0, 0, 0, 0.25);">
        <div class="w-full bg-white py-8">
          <div class="flex px-8 w-full items-center">
            <div class="pr-4 cursor-pointer" @click="ShowPlus = true">
              <img src="plus.svg" alt="">
            </div>
            <div class="w-full">
              <input type="text" placeholder="Pesan" class=" text-slate-600 font-medium text-sm w-full border-blue-500 border px-4 py-2 rounded-full placeholder:text-slate-500 focus:border-blue-700 transition-all duration-300 focus:outline-none" style="background-color: rgba(242, 242, 242, 1)">
            </div>
            <div class="pl-4">
              <img src="mic.svg" alt="">
            </div>
          </div>
        </div>
      </div>
      <PlusApp :show-plus="ShowPlus" @close="ShowPlus =false" />
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      ShowPlus: false
    }
  }
}
</script>
