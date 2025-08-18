<script lang="ts" setup>
  const title = ref('วิทยาลัยเทคนิคตราด')
</script>

<template>
  <Head>
    <Title>{{ title }}</Title>
    <Meta name="description" :content="title" />
    <Style>
    body { background-color: green; }
    </Style>
  </Head>

  <div class="font-[Sarabun] bg-white py-14 px-6 sm:px-12 bg-gradient-to-r from-pink-50 via-pink-50 to-blue-100">
    <div class="max-w-screen-xl mx-auto shadow-2xl rounded-xl p-4">
      <div class="max-w-screen-md font-[Kanit]">
          <h2 class="text-[#801810] xl:text-5xl md:text-5xl text-4xl font-bold !leading-tight">สาส์นจากผู้อำนวยการ</h2>
      </div>

      <div class="grid lg:grid-cols-2 gap-16 lg:gap-12 mt-6">
        <div>
          <p class="text-slate-600 md:text-md leading-relaxed mx-auto max-w-screen-xl">
            ขอขอบคุณผู้ปกครองนักเรียน นักศึกษาที่ให้ความไว้วางใจวิทยาลัย ที่ให้ความร่วมมืออย่างดีในกิจกรรมต่างๆ ของวิทยาลัยฯ
            ขอขอบใจนักเรียนนักศึกษาทุกคนที่ปฏิบัติตนอยู่ในระเบียบของวิทยาลัย อยู่ในโอวาทของทุกคน เป็นนักเรียนนักศึกษาที่ วิทยาลัยภาคภูมิใจ.
          </p>

          <div class="max-w-screen-md mt-2">
            <h2 class="xl:text-xl md:text-xl text-xl font-sm !leading-tight text-[#801810]">
              “เทคนิคตราดโฉมใหม่ ใส่ใจบุตรหลาน จัดการศึกษา เพื่อการมีงานทำ”</h2>
          </div>

          <div class="mt-12 flex gap-6 items-center flex-wrap">
            <button type='button' class="bg-[#55F5A3] hover:bg-green-400 transition-all text-slate-900 font-semibold text-[15px] rounded-full px-6 py-3 cursor-pointer">Getting
              Started
            </button>
            <a href="javascript:void(0)" class="text-slate-900 text-[15px] font-semibold underline max-sm:block whitespace-nowrap">API
              Documentation
            </a>
          </div>

          <div class="mt-12 flex flex-wrap gap-x-2 gap-y-2">
            <a href="https://rms.trattc.ac.th/?p=login" target="_blank">
              <img src="~/assets/img/rms.png" class="shrink-0 w-48 h-32 shadow-2xl rounded-md p-2 hover:scale-[1.05] transition-all" alt="brand-logo1" />
            </a>

            <a href="https://std2018.vec.go.th/web/" target="_blank">
              <img src="~/assets/img/std02.png" class="w-48 h-32 shrink-0 shadow-2xl rounded-md p-2 hover:scale-[1.05] transition-all" alt="brand-logo2" />
            </a>

            <a href="https://admission.vec.go.th/web/Login.htm?mode=index" target="_blank">
              <img src="~/assets/img/std_register.png" class="w-48 h-32 shrink-0 shadow-2xl rounded-md p-2 hover:scale-[1.05] transition-all" alt="brand-logo3" />
            </a>
            </div>
        </div>

        <div class="max-w-full">
            <img src="~/assets/img/child2568.jpg" class="shrink-0 shadow-2xl rounded-md object-contain hover:scale-[1.05] transition-all" />
        </div>
      </div>
    </div>
  </div>

  <div class="font-[Sarabun] min-h-screen bg-white px-6 sm:px-12 bg-gradient-to-r from-pink-50 via-pink-50 to-blue-100 py-2 mb-10">
    <div class="mx-auto sm:max-w-6xl md:max-w-7xl max-w-md pl-0 md:pl-0 shadow-2xl rounded-xl">
      <h2 class="text-2xl sm:text-3xl font-bold text-slate-900 mb-2 sm:mb-2 mt-5 p-4">ข่าวล่าสด</h2>

      <div class="grid grid-cols-1 sm:grid-cols-3 md:grid-cols-4 gap-2 sm:gap-4 p-4">

        <div class="bg-white flex flex-col rounded-lg overflow-hidden shadow-md hover:scale-[1.02] transition-all">
          <div class="aspect-[3/2] cursor-pointer">
            <img src="https://readymadeui.com/Imagination.webp" class="w-full h-full object-cover" alt="Card image" />
          </div>

          <div class="p-6">
            <h3 class="text-slate-900 text-xl font-semibold">Heading</h3>
            <p class="mt-3 text-md text-slate-500 leading-relaxed">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum sunt consequuntur necessitatibus, eveniet
              eligendi ullam?
            </p>
            <button type="button" class="mt-6 px-5 py-2.5 rounded-lg text-white text-sm font-medium tracking-wider border-none outline-none bg-blue-600 
            hover:bg-blue-700 active:bg-blue-600 cursor-pointer">
              View
            </button>
          </div>
        </div>

         <div class="bg-white flex flex-col rounded-lg overflow-hidden shadow-md hover:scale-[1.02] transition-all">
          <div class="aspect-[3/2] cursor-pointer">
            <img src="https://readymadeui.com/Imagination.webp" class="w-full h-full object-cover" alt="Card image" />
          </div>

          <div class="p-6">
            <h3 class="text-slate-900 text-xl font-semibold">Heading</h3>
            <p class="mt-3 text-md text-slate-500 leading-relaxed">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum sunt consequuntur necessitatibus, eveniet
              eligendi ullam?
            </p>
            <button type="button" class="mt-6 px-5 py-2.5 rounded-lg text-white text-sm font-medium tracking-wider border-none outline-none bg-blue-600 
            hover:bg-blue-700 active:bg-blue-600 cursor-pointer">
              View
            </button>
          </div>
        </div>

         <div class="bg-white flex flex-col rounded-lg overflow-hidden shadow-md hover:scale-[1.02] transition-all">
          <div class="aspect-[3/2] cursor-pointer">
            <img src="https://readymadeui.com/Imagination.webp" class="w-full h-full object-cover" alt="Card image" />
          </div>

          <div class="p-6">
            <h3 class="text-slate-900 text-xl font-semibold">Heading</h3>
            <p class="mt-3 text-md text-slate-500 leading-relaxed">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum sunt consequuntur necessitatibus, eveniet
              eligendi ullam?
            </p>
            <button type="button" class="mt-6 px-5 py-2.5 rounded-lg text-white text-sm font-medium tracking-wider border-none outline-none bg-blue-600 
            hover:bg-blue-700 active:bg-blue-600 cursor-pointer">
              View
            </button>
          </div>
        </div>

         <div class="bg-white flex flex-col rounded-lg overflow-hidden shadow-md hover:scale-[1.02] transition-all">
          <div class="aspect-[3/2] cursor-pointer">
            <img src="https://readymadeui.com/Imagination.webp" class="w-full h-full object-cover" alt="Card image" />
          </div>

          <div class="p-6">
            <h3 class="text-slate-900 text-xl font-semibold">Heading</h3>
            <p class="mt-3 text-md text-slate-500 leading-relaxed">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum sunt consequuntur necessitatibus, eveniet
              eligendi ullam?
            </p>
            <button type="button" class="mt-6 px-5 py-2.5 rounded-lg text-white text-sm font-medium tracking-wider border-none outline-none bg-blue-600 
            hover:bg-blue-700 active:bg-blue-600 cursor-pointer">
              View
            </button>
          </div>
        </div>

         <div class="bg-white flex flex-col rounded-lg overflow-hidden shadow-md hover:scale-[1.02] transition-all">
          <div class="aspect-[3/2] cursor-pointer">
            <img src="https://readymadeui.com/Imagination.webp" class="w-full h-full object-cover" alt="Card image" />
          </div>

          <div class="p-6">
            <h3 class="text-slate-900 text-xl font-semibold">Heading</h3>
            <p class="mt-3 text-md text-slate-500 leading-relaxed">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum sunt consequuntur necessitatibus, eveniet
              eligendi ullam?
            </p>
            <button type="button" class="mt-6 px-5 py-2.5 rounded-lg text-white text-sm font-medium tracking-wider border-none outline-none bg-blue-600 
            hover:bg-blue-700 active:bg-blue-600 cursor-pointer">
              View
            </button>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<style>

</style>