<template>
  <div>
    <div class="max-w-xl w-full mx-auto">
      <div class="container">
        <img src="/vectora.png" class="w-full">
        <div class="flex flex-row w-full  bg-white shadow-md">
          <div class="py-5 px-5">
            <img src="/profil.svg" alt="" class="w-20 h-20">
          </div>
          <div class="py-5 px-8 w-full">
            <h2 class="font-bold text-xl">
              {{ $nuxt.$cookiz.get('auth').user.first_name }}   {{ $nuxt.$cookiz.get('auth').user.last_name }}
            </h2>
            <div class="flex justify-between">
              <h2 class="font-medium text-gray-500">
                ID: {{ $nuxt.$cookiz.get('auth').user.id_user }}
              </h2>
              <div class="w-14 h-5 rounded-full" style="background: linear-gradient(90deg, #C4A7F4 0%, #B7B5F4 35.42%, #A8C8F5 63.02%, #95DEF7 100%);">
                <p class="text-white text-center font-semibold text-sm">
                  {{ $nuxt.$cookiz.get('auth').user.position }}
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="px-4 py-4 bg-white shadow-md h-screen">
          <div class="w-full h-max rounded-md bg-blue-100 shadow-lg">
            <div class="flex border-b px-4 py-4">
              <img src="acc.svg" alt="">
              <p class="pl-4 ">
                Akun
              </p>
            </div>
            <div class="flex px-4 py-4">
              <img src="key.svg" alt="">
              <p class="pl-4">
                Ganti Password
              </p>
            </div>
          </div>
          <div class="pt-4">
            <div class="w-full h-max rounded-md bg-blue-100 shadow-lg">
              <div class="flex border-b px-4 py-4">
                <img src="tentang.svg" alt="">
                <p class="pl-4 ">
                  Tentang Kami
                </p>
              </div>
              <div class="flex px-4 py-4">
                <img src="privasi.svg" alt="">
                <p class="pl-4">
                  Kebijakan Privasi
                </p>
              </div>
            </div>
          </div>
          <div class="pt-4">
            <div class="w-full h-max rounded-md bg-blue-100 shadow-lg">
              <div class="flex border-b px-4 py-4" @click="logout">
                <img src="keluar.svg" alt="">
                <p class="pl-4 ">
                  Keluar
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="max-w-xl w-full mx-auto border-t">
      <div class="w-full bg-white shadow-md py-4">
        <div>
          <ul class="flex justify-between px-14 items-center">
            <li>
              <router-link to="/homeapp">
                <img src="/home1.svg" class="pl-2">
                <div class="text-gray-400 text-center">
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
              <router-link to="/chat">
                <img src="/chat.png" alt="">
                <span class="text-gray-400">Chat</span>
              </router-link>
            </li>
            <li>
              <router-link to="/proflogin">
                <img src="/profil2.svg" class="pl-2">
                <span class="text-blue-500">Profile</span>
              </router-link>
            </li>
          </ul>
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
  },
  methods: {
    logout () {
      this.$nuxt.removeAll()
      this.$router.replace('/login')
      this.$toast.success(' Log out berhasil')
    }
  }
}
</script>
