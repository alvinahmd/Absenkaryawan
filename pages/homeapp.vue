<template>
  <div class="max-w-xl w-full mx-auto">
    <div class="flex flex-row py-5 px-4 bg-white shadow-lg my-0 mx-auto ">
      <div class="mx-auto items-center">
        <img src="/manggala.svg">
      </div>
      <a href="/notifikasiapp">
        <img src="/lonceng2.svg">
      </a>
    </div>
    <div class="">
      <table class="items-center w-full border">
        <template v-for="detail in list">
          <tr v-for="(home, i) in detail.presence__user__detail" :key="i" class="border-b text-white rounded-t-xl" style="background-color: rgba(242, 251, 255, 1)">
            <th class="py-4 pl-4">
              <img src="/app/sampah2.svg" class="w-full cursor-pointer" @click="hapus(home.id)">
            </th>
            <th class="text-gray-600">
              {{ (home) ? home.presence_at : null }}
            </th>
            <th class="text-gray-600">
              {{ detail && detail.presence.date_presence }}
            </th>
            <th class="text-gray-600">
              {{ (home) ? home.presence_at : null }}
            </th>
          </tr>
        </template>
      </table>
    </div>
    <div class="my-0 mx-auto min-h-full max-w-screen-sm">
      <div class="container">
        <div class="relative  flex flex-row py-2 px-4 bg-white shadow-lg">
          <div class=" cursor-pointer flex list-none flex-col flex-wrap border-b-0 pl-0 md:flex-row" @click="ShowCheck = true">
            <p class="font-medium px-20 mx-auto">
              Check In
            </p>
          </div>
          <div class="font-medium px-20 mx-auto cursor-pointer" @click="ShowOut = true">
            Check out
          </div>
          <a href="/riwayatapp">
            <img src="/timer.svg" class="pr-2">
          </a>
        </div>
        <div class="py-8 px-24 cursor-pointer">
          <div class="flex justify-center">
            <button class=" border-purple-800 w-48 h-48 rounded-full border-8 focus:ring-8 focus:ring-purple-400 focus:border-none transition-none" @click="ShowCheck = true">
              <p class="text-lg font-semibold " style="color: rgba(0, 117, 255, 1)">
                Check in
              </p>
              <!-- <div class="text-base font-medium" style="color: rgba(68, 68, 68, 1)">
                7.40 PM
              </div> -->
            </button>
          </div>
        </div>
        <div class="my-0 mx-auto max-w-xl translate-y-6 pt-4">
          <div class="w-full bg-white  shadow-md py-4">
            <div>
              <ul class="flex justify-between px-14 items-center">
                <li>
                  <router-link to="/">
                    <img src="/app/home.svg" class="pl-2">
                    <div class="text-blue-500 text-center">
                      Home
                    </div>
                  </router-link>
                </li>
                <li class="text-white">
                  <a href="https://meet.google.com/pwg-zcyr-bcp">
                    <img src="/app/meet.svg" alt="">
                    <span class="text-gray-400 ">Meet</span>
                  </a>
                </li>
                <li>
                  <router-link to="/chat">
                    <img src="/app/pesan.svg" alt="">
                    <span class="text-gray-400">Chat</span>
                  </router-link>
                </li>
                <li>
                  <router-link to="/proflogin">
                    <img src="/app/profil.svg" class="pl-2">
                    <span class="text-gray-400">Profile</span>
                  </router-link>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <CheckinApp :show-check="ShowCheck" @close="ShowCheck =false" />
      <CheckotApp :show-out="ShowOut" @close="ShowOut =false" />
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      ShowCheck: false,
      ShowOut: false,
      list: null
    }
  },
  mounted () {
    this.getData()
  },
  methods: {
    async getData () {
      try {
        await this.$axios.$get('/api/list', {
          headers: { 'ngrok-skip-browser-warning': '123123' }
        })
          .then((res) => {
            this.list = res.message
          })
      } catch (error) {
        alert(alert.response.data.message)
      }
    },
    async hapus (id) {
      try {
        await this.$axios.$delete('https://9e25-2001-448a-5040-80a5-31cf-64a0-6b7f-5326.ngrok-free.app/api/userdetail/' + id, {
          headers: { 'ngrok-skip-browser-warning': '123123' }
        })
          .then((res) => {
            console.log('res', res)
            this.$router.replace('homeapp')
            this.$toast.success('Hapus berhasil')
          })
      } catch (error) {
        alert(error.response.data.message)
        console.log(error)
      }
    }
  }
}
</script>
