<template>
  <div>
    <div class="max-w-screen-sm mx-auto h-screen shadow-xl">
      <img src="/img.png" class="w-screen ">
      <h1 class="pl-72 text-blue-600 font-bold 4xl">
        Buat Akun
      </h1>
      <div class="flex justify-center items-center pt-4">
        <div>
          <div class="relative">
            <div for="text" class="mb-4 pl-1 text-blue-700 font-bold">
              ID
            </div>
            <input
              v-model="inputid"
              type="text"
              placeholder="Masukkan ID / Nomor Karyawan"
              class="w-96 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
            >
          </div>
          <!-- Password input -->
          <div class="relative">
            <div for="password" class="mb-1 pl-1 text-blue-700 font-bold">
              Password
            </div>
            <input
              v-if="showPassword"
              v-model="inputPass"
              type="text"
              name="password"
              placeholder="Masukkan Password"
              class="w-96 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
            >
            <input
              v-else
              v-model="inputPass"
              type="password"
              name="password"
              placeholder="Password"
              class="w-96 px-4 py-2 mb-4 text-black transition duration-500 ease-in-out transform bg-gray-100 border-transparent rounded-lg mr-4text-base focus:border-gray-500 focus:bg-white focus:outline-none focus:shadow-outline focus:ring-2"
            >
            <div class="absolute inset-y-0 right-0 flex items-center text-sm leading-5 pr-5 pt-4 text-neutral-dark cursor-pointer" @click="toggleShow">
              <span v-if="showPassword">
                <svg
                  width="26"
                  height="24"
                  viewBox="0 0 26 13"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path d="M24.853 5.80498C24.9861 5.94021 25.1206 6.07688 25.257 6.21486C24.8353 6.56669 24.4249 6.92761 24.0207 7.28307C23.7794 7.49533 23.5402 7.70565 23.3022 7.91091C22.5218 8.58388 21.7318 9.2224 20.8387 9.77797C19.068 10.8794 16.8561 11.6772 13.4937 11.6772C7.09369 11.6772 3.31137 8.78335 0.726526 6.26775C0.734986 6.26004 0.743442 6.25233 0.751895 6.24462C2.40883 4.73393 3.91474 3.36094 5.75854 2.32869C7.73649 1.22132 10.1198 0.5 13.4937 0.5C16.8672 0.5 19.0768 1.22097 20.8387 2.31697C22.3368 3.24886 23.5242 4.45504 24.853 5.80498Z" stroke="black" />
                  <circle cx="13.1643" cy="6.25315" r="5.42405" stroke="black" />
                  <circle cx="13.1642" cy="6.25327" r="2.63291" fill="black" />
                </svg>
              </span>
              <span v-if="!showPassword">
                <svg
                  width="26"
                  height="24"
                  viewBox="0 0 26 24"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path d="M24.853 11.805C24.9861 11.9402 25.1206 12.0769 25.257 12.2149C24.8353 12.5667 24.4249 12.9276 24.0207 13.283C23.7794 13.4953 23.5402 13.7056 23.3022 13.9109C22.5218 14.5839 21.7318 15.2224 20.8387 15.778C19.068 16.8794 16.8561 17.6772 13.4937 17.6772C7.09369 17.6772 3.31137 14.7833 0.726526 12.2678C0.734986 12.26 0.743442 12.2523 0.751895 12.2446C2.40883 10.7339 3.91474 9.36094 5.75854 8.32869C7.73649 7.22132 10.1198 6.5 13.4937 6.5C16.8672 6.5 19.0768 7.22097 20.8387 8.31697C22.3368 9.24887 23.5242 10.455 24.853 11.805Z" stroke="black" />
                  <circle cx="13.1643" cy="12.2532" r="5.42405" stroke="black" />
                  <circle cx="13.1642" cy="12.2533" r="2.63291" fill="black" />
                  <path d="M22 1L7 23.5" stroke="white" stroke-linecap="round" />
                  <path d="M21 1L6 23.5" stroke="black" stroke-linecap="round" />
                </svg>
              </span>
            </div>
          </div>
          <!-- Submit button -->
          <button
            class="inline-block w-full rounded bg-blue-600 px-7 pb-2.5 pt-3 items-center text-center text-sm font-medium uppercase leading-normal text-white shadow-[0_4px_9px_-4px_#3b71ca] transition duration-150 ease-in-out hover:bg-primary-600 hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:bg-primary-600 focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:outline-none focus:ring-0 active:bg-primary-700 active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] dark:shadow-[0_4px_9px_-4px_rgba(59,113,202,0.5)] dark:hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] dark:focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] dark:active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)]"
            data-te-ripple-init
            data-te-ripple-color="light"
            @click="login()"
          >
            Masuk
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      inputPasswd: false,
      showPassword: false,
      password: null,
      inputid: null,
      inputPass: null
    }
  },
  computed: {
    buttonLabel () {
      return (this.showPassword) ? 'Hide' : 'Show'
    }
  },
  methods: {
    toggleShow () {
      this.showPassword = !this.showPassword
    },
    async login () {
      console.log('fdf  df')
      try {
        await this.$axios.$post('/api/login',
          {
            headers: { 'ngrok-skip-browser-warning': '123123' },
            id_user: this.inputid,
            password: this.inputPass
          }).then((res) => {
          this.$cookiz.set('auth', res)
          this.$router.replace('/homeapp')
          this.$toast.success(' Login berhasil')
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
