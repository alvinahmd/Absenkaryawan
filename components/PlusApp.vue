<!-- eslint-disable no-irregular-whitespace -->
<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <div v-if="ShowPlus" class="fixed top-0 left-0 flex justify-center items-end w-screen h-full">
      <div class="fixed top-0 left-0 w-screen h-screen duration-700" @click="$emit('close')" />
      <div class="w-96 max-h-screen" style="z-index: 1;">
        <div>
          <div class="-translate-y-28 -translate-x-9">
            <div class=" bg-white shadow-lg rounded-lg">
              <div class="flex pl-4 py-2 border-b-2 items-center">
                <svg width="22" height="19" viewBox="0 0 22 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M14.1278 10.2394C14.1278 12.287 12.4679 13.9469 10.4203 13.9469C8.37277 13.9469 6.71289 12.287 6.71289 10.2394C6.71289 8.19186 8.37277 6.53198 10.4203 6.53198C12.4679 6.53198 14.1278 8.19186 14.1278 10.2394Z" stroke="#0075FF" stroke-width="2" />
                  <path d="M14.9808 2.78903L15.2779 3.11111H15.716H19.0754C19.6925 3.11111 20.1948 3.61712 20.1948 4.22222V16.8889C20.1948 17.494 19.6925 18 19.0754 18H2.11949C1.50232 18 1 17.494 1 16.8889V4.22222C1 3.61712 1.50232 3.11111 2.11949 3.11111H5.47887H5.9194L6.21674 2.78606L7.51688 1.3647C7.73312 1.13379 8.04033 1 8.35077 1H12.8437C12.9984 1.00013 13.1513 1.03239 13.2926 1.0946C13.4339 1.15684 13.5603 1.24763 13.6639 1.36093L13.6639 1.36094L13.6668 1.36403L14.9808 2.78903Z" stroke="#0075FF" stroke-width="2" />
                </svg>
                <p class="text-base font-medium pl-4" style="color: rgba(68, 68, 68, 1)">
                  Kamera
                </p>
              </div>
              <div class="flex pl-4 py-2 border-b-2">
                <svg width="22" height="18" viewBox="0 0 22 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M1 14L5.95043 10.8497C6.2845 10.6371 6.71254 10.6417 7.04201 10.8613L8.88455 12.0897C9.25026 12.3335 9.7323 12.3099 10.0725 12.0316L14.3668 8.5181C14.7351 8.21671 15.2649 8.21671 15.6332 8.5181L20.5 12.5" stroke="#0075FF" stroke-width="2" />
                  <path d="M1 16V2C1 1.44772 1.44772 1 2 1H20C20.5523 1 21 1.44772 21 2V16C21 16.5523 20.5523 17 20 17H2C1.44772 17 1 16.5523 1 16Z" stroke="#0075FF" stroke-width="2" stroke-linecap="round" />
                  <circle cx="6" cy="6" r="1.5" stroke="#0075FF" />
                </svg>
                <p class="text-base font-medium pl-4" style="color: rgba(68, 68, 68, 1)">
                  Perpustakaan
                </p>
              </div>
              <div class="flex pl-4 py-2 border-b-2">
                <svg width="18" height="24" viewBox="0 0 18 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M9.84211 1H10.6896C10.9557 1 11.2108 1.10602 11.3984 1.29459L14.0526 3.96154L16.7088 6.63048C16.8953 6.81787 17 7.0715 17 7.33589V8.61538M9.84211 1H2C1.44772 1 1 1.44772 1 2V22C1 22.5523 1.44772 23 2 23H16C16.5523 23 17 22.5523 17 22V8.61538M9.84211 1V7.61539C9.84211 8.16767 10.2898 8.61538 10.8421 8.61538H17" stroke="#0075FF" stroke-width="2" />
                </svg>
                <p class="text-base font-medium pl-4" style="color: rgba(68, 68, 68, 1)">
                  Dokumen
                </p>
              </div>
              <div class="flex pl-4 py-2">
                <svg width="17" height="24" viewBox="0 0 17 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M16 8.4C16 10.4813 15.0222 13.5339 13.4668 16.3715C12.0199 19.0112 10.1987 21.2352 8.47297 22.275C6.54905 21.2441 4.72896 19.0268 3.34232 16.3871C1.86238 13.5698 1 10.5066 1 8.4C1 4.32422 4.34667 1 8.5 1C12.6533 1 16 4.32422 16 8.4Z" stroke="#0075FF" stroke-width="2" />
                  <circle cx="8.5" cy="8.5" r="3" stroke="#0075FF" />
                </svg>
                <p class="text-base font-medium pl-4" style="color: rgba(68, 68, 68, 1)">
                  Lokasi
                </p>
              </div>
            </div>
            <div class="pt-2">
              <div class="bg-white shadow-lg rounded-xl px-4 py-2 cursor-pointer" @click="$emit('close')">
                <p class="text-blue-500 font-medium text-lg text-center">
                  Batal
                </p>
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
    ShowPlus: {
      type: Boolean,
      default: false
    }
  }
}
</script>
