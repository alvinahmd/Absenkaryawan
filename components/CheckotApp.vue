<!-- eslint-disable no-irregular-whitespace -->
<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <div v-if="ShowOut" class="fixed top-0 left-0 flex justify-center items-end w-screen h-full">
      <div class="fixed top-0 left-0 w-screen h-screen duration-700" @click="$emit('close')" />
      <div class="w-full max-w-xl bg-white max-h-screen" style="z-index: 1;">
        <div>
          <div class="border-b">
            <div class="flex flex-row py-5 px-4 rounded-t-xl bg-white shadow-lg">
              <a href="">
                <svg width="11" height="19" viewBox="0 0 11 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M9 2L3 9.1875L9 17" stroke="#0075FF" stroke-width="4" stroke-linecap="round" />
                </svg>
              </a>
              <h1 class="font-medium text-base mx-auto" style="color:rgba(50, 11, 78, 1)">
                Check Out
              </h1>
            </div>
          </div>
          <div class="bg-white shadow-lg">
            <div class="px-8">
              <div class="flex flex-row w-full">
                <div class="pt-8">
                  <h1 class="font-semibold text-sm" style="color: rgba(68, 68, 68, 1)">
                    Dikerjakan
                  </h1>
                  <textarea v-model="inputdikerjakan" type="text" placeholder="Apa yang anda kerjakan hari ini" class=" bg-slate-100 px-2 h-64 w-56 rounded-lg outline-none transition-all placeholder:text-sm placeholder:text-slate-300" />
                </div>
                <div class="flex-col">
                  <div class="px-8 pt-8 flex">
                    <h1 class="-translate-y-2 text-base pr-2 font-semibold" style="color: rgba(68, 68, 68, 1)">
                      Foto:
                    </h1>
                    <label for="inputFoto">
                      <div v-if="!avatarPV" class=" w-16 h-24 bg-slate-100 rounded-md cursor-pointer" />
                      <img v-if="avatarPV" :src="avatarPV" alt="" class=" w-16 h-24 object-cover">
                    </label>
                    <input id="inputFoto" class="hidden" type="file" @change="showpreview">
                  </div>
                  <div class="px-8 py-8 flex">
                    <h1 class="-translate-y-2 text-base pr-2 font-semibold" style="color: rgba(68, 68, 68, 1)">
                      Location:
                    </h1>
                    <input v-model="inputlokasi" type="text" class=" px-2 w-40 h-9 bg-slate-100 rounded-md outline-none placeholder:text-center placeholder:text-blue-500 placeholder:text-xs placeholder:font-medium" placeholder="Kirim Live Lokasi Anda">
                  </div>
                  <div class="pl-8">
                    <h1 class="font-semibold text-base" style="color: rgba(68, 68, 68, 1)">
                      Hasil Yang Dikerjakan
                    </h1>
                    <input v-model="inputhasil" placeholder="Masukan Link G-drive" class=" bg-slate-100 px-2 h-10 w-60 rounded-lg outline-none placeholder:text-center placeholder:text-xs placeholder:font-medium placeholder:text-blue-500">
                  </div>
                  <div class="pl-8">
                    <h1 class="font-semibold text-base" style="color: rgba(68, 68, 68, 1)">
                      Hasil Yang Dikerjakan
                    </h1>
                    <input v-model="inputhasil2" placeholder="Masukan Link G-drive" class=" bg-slate-100 px-2 h-10 w-60 rounded-lg outline-none placeholder:text-center placeholder:text-xs placeholder:font-medium placeholder:text-blue-500">
                  </div>
                </div>
              </div>
              <div class="py-8">
                <button class="rounded-lg w-full bg-blue-600 py-4 font-semibold text-white text-base hover:opacity-70 transition-all focus:ring-4 focus:ring-blue-200 focus:opacity-100" @click="checkotapp">
                  Upload
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    // eslint-disable-next-line vue/prop-name-casing
    ShowOut: {
      type: Boolean,
      default: false
    }
  },
  data () {
    return {
      inputFoto: null,
      avatarPV: null,
      inputdikerjakan: null,
      inputlokasi: null,
      inputhasil: null,
      inputhasil2: null
    }
  },
  methods: {
    showpreview (e) {
      const file = e.target.files[0]
      this.avatarPV = URL.createObjectURL(file)
      this.inputFoto = file
    },
    async checkotapp () {
      try {
        const formData = new FormData()
        formData.append('photo', this.inputFoto)
        formData.append('latitude', this.inputdikerjakan)
        formData.append('longitude', this.inputlokasi)
        formData.append('finished_task', this.inputhasil)
        formData.append('description', this.inputhasil2)
        console.log(this.inputFoto)
        await this.$axios.$post('/api/checkout', formData,
          {
            headers: {
              'ngrok-skip-browser-warning': '123123'
            }
          }
        ).then((res) => {
          // this.$cookiz.set('auth', res)
          // this.$router.replace('/beranda')
          this.$toast.success(' Checkout berhasil')
          // this.$cookiz.get('user')
          // this.$cookiz.remove('user')
        })
      } catch (error) {
        alert(error.response.data.message)
      }
    }
  }
}
</script>
