<template>
  <div>
    <div class="mx-auto max-w-4xl">
      <div class="shadow-lg bg-white border-b-2">
        <div class="py-4 px-4">
          <img src="/manggala.svg" class="w-72">
        </div>
      </div>
      <div class="bg-white w-full h-full shadow-lg border-b-2">
        <div class="px-4 py-4">
          <div class="relative">
            <div>
              <div class="w-80 h-max rounded-lg" style="background-color: rgba(242, 251, 255, 1)">
                <div class="px-2 py-2">
                  <div class="flex justify-between">
                    <h1 class="font-medium text-base" style="color:rgba(68, 68, 68, 1)">
                      Alvin Top Ahmad
                    </h1>
                    <span class="w-14 h-7 text-center text-white font-semibold text-sm rounded-full" style="background: linear-gradient(90deg, #C4A7F4 0%, #B7B5F4 35.42%, #A8C8F5 63.02%, #95DEF7 100%">
                      <p class="translate-y-1">
                        FE Dev
                      </p>
                    </span>
                  </div>
                  <div class="font-bold text-sm" style="color: rgba(155, 155, 155, 1)">
                    <p>
                      ID:234598
                    </p>
                    <p>
                      alvin@gmail.com
                    </p>
                    <p>
                      098733927
                    </p>
                    <div class="flex justify-end text-base">
                      Magang
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="bg-white shadow-lg px-4 py-4">
        <vue-good-table
          :columns="columns"
          :rows="rows"
        >
          />
        </vue-good-table>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      columns: [
        {
          label: 'Tanggal',
          field: 'name'
        },
        {
          label: 'lokasi',
          field: 'location'
        },
        {
          label: 'Checkin',
          field: 'in'
        },
        {
          label: 'Yang di kerjakan',
          field: 'dikerjakan'
        },
        {
          label: 'Checkout',
          field: 'out'
        },
        {
          label: 'Yang di kerjakan',
          field: 'dikerjakann'
        },
        {
          label: 'Keterangan',
          field: 'desc'
        }
      ],
      rows: [
        { id: 1, name: '1/12/2022', location: 'PT.Manggala Teknologi,Tegowangi,kec.Pare.kab Kediri', in: '07.38', dikerjakan: 'Membuat halaman Login admi  dan login karyawan pada apk', out: '17.11', dikerjakann: 'Membuat halaman Login admi  dan login karyawan pada apk', desc: 'Hadir' },
        { id: 2, name: '1/12/2022', location: 'PT.Manggala Teknologi,Tegowangi,kec.Pare.kab Kediri', in: '07.38', dikerjakan: 'Membuat halaman Login admi  dan login karyawan pada apk', out: '17.11', dikerjakann: 'Membuat halaman Login admi  dan login karyawan pada apk', desc: 'Hadir' },
        { id: 3, name: '1/12/2022', location: 'PT.Manggala Teknologi,Tegowangi,kec.Pare.kab Kediri', in: '07.38', dikerjakan: 'Membuat halaman Login admi  dan login karyawan pada apk', out: '17.11', dikerjakann: 'Membuat halaman Login admi  dan login karyawan pada apk', desc: 'Hadir' },
        { id: 4, name: '1/12/2022', location: 'PT.Manggala Teknologi,Tegowangi,kec.Pare.kab Kediri', in: '07.38', dikerjakan: 'Membuat halaman Login admi  dan login karyawan pada apk', out: '17.11', dikerjakann: 'Membuat halaman Login admi  dan login karyawan pada apk', desc: 'Hadir' },
        { id: 5, name: '1/12/2022', location: 'PT.Manggala Teknologi,Tegowangi,kec.Pare.kab Kediri', in: '07.38', dikerjakan: 'Membuat halaman Login admi  dan login karyawan pada apk', out: '17.11', dikerjakann: 'Membuat halaman Login admi  dan login karyawan pada apk', desc: 'Hadir' }
      ]
    }
  }
}
</script>
