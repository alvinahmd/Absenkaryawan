<template>
  <div>
    <div class="max-w-xl w-full mx-auto">
      <div class="relative flex flex-row py-5 px-4 bg-white shadow-lg">
        <router-link to="/proflogin">
          <img src="/back.svg">
        </router-link>
        <h1 class="font-bold mx-auto" style="color:rgba(68, 68, 68, 1)">
          Akun
        </h1>
      </div>
      <div class="container bg-white w-11/12 h-90 items-center mx-auto">
        <div class="border-t solid " style="color:rgba(188, 188, 188, 1)">
          <div class=" rounded-xl shadow-md bg-slate-100 items-center pt-3 pb-3 pl-4">
            <div class="px-5 flex gap-4 cursor-pointer" @click="showLogin = true">
              <h1 class="text-lg font-semibold" style="color:rgba(68, 68, 68, 1)">
                fransciexho steinlie
              </h1>
            </div>
          </div>
          <div class="border b solid" />
          <div class="rounded-xl shadow-md bg-slate-100 items-center pt-3 pb-3 pl-4">
            <div class="px-5 flex gap-4">
              <h1 class="text-lg font-semibold" style="color:rgba(68, 68, 68, 1)">
                ID:236765
              </h1>
            </div>
          </div>
          <div class="border b solid" />
          <div class="rounded-xl shadow-md bg-slate-100  items-center pt-3 pb-3 pl-4">
            <div class="px-5 flex gap-4">
              <a href="/verif">
                <h1 class="text-lg font-semibold" style="color:rgba(68, 68, 68, 1)">
                  fransciesco.steinlie@gmail.com
                </h1>
              </a>
            </div>
          </div>
          <div class="border b solid" />
          <div class="rounded-xl shadow-md bg-slate-100 items-center pt-3 pb-3 pl-3">
            <div class="px-5 flex gap-4">
              <a href="/kebijakanprivasi">
                <h1 class="text-lg font-semibold" style="color:rgba(68, 68, 68, 1)">
                  +62 877 6604 4919
                </h1>
              </a>
            </div>
          </div>
          <div class="border b solid" />
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
