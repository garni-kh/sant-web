<template>
  <!-- Page Title:Begin -->
  <section class="max-w-[1113px] mx-auto mb-[80px]">
    <h1 class="text-primary-500 text-[32px] leading-[50px] font-bold text-center">تماس با ما</h1>
  </section>
  <!-- Page Title:End -->

  <!-- Contact Detail:Begin -->
  <section
    class="max-w-[1113px] mx-auto pb-[56px] mb-[56px] border-b-[1px] border-[#D3D1D1] px-[40px] md:px-0"
  >
    <div class="grid grid-cols-2 flex-row-reverse">
      <div class="col-span-2 md:col-span-1">
        <div class="flex flex-col space-y-[30px]">
          <div class="grid grid-cols-2">
            <p class="text-[16px] leading-[31.25px] text-primary-500 font-semibold">
              آدرس دفتر مرکزی:
            </p>
            <p class="text-[14px] leading-[28.52px] text-[#403D3D] font-normal">
              75 کیلومتری اتوبان ساوه تهران ناحیه صنعتی پرندک
            </p>
          </div>
          <div class="grid grid-cols-2">
            <p class="text-[16px] leading-[31.25px] text-primary-500 font-semibold">
              آدرس کارخانه:
            </p>
            <p class="text-[14px] leading-[28.52px] text-[#403D3D] font-normal">
              75 کیلومتری اتوبان ساوه تهران ناحیه صنعتی پرندک
            </p>
          </div>
          <div class="grid grid-cols-2">
            <p class="text-[16px] leading-[31.25px] text-primary-500 font-semibold">
              تلفن دفتر مرکزی:
            </p>
            <p class="text-[14px] leading-[28.52px] text-[#403D3D] font-normal">۰۲۱۸۸۹۱۸۶۷۸-۰۲</p>
          </div>
          <div class="grid grid-cols-2">
            <p class="text-[16px] leading-[31.25px] text-primary-500 font-semibold">
              تلفن کارخانه:
            </p>
            <p class="text-[14px] leading-[28.52px] text-[#403D3D] font-normal">۰۲۱۸۸۹۱۸۶۷۸-۰۲</p>
          </div>
          <div class="grid grid-cols-2">
            <p class="text-[16px] leading-[31.25px] text-primary-500 font-semibold">فکس:</p>
            <p class="text-[14px] leading-[28.52px] text-[#403D3D] font-normal">۰۲۱۸۸۹۱۸۶۷۸-۰۲</p>
          </div>
          <div class="grid grid-cols-2">
            <p class="text-[16px] leading-[31.25px] text-primary-500 font-semibold">
              تلفن راهکارهای خاص:
            </p>
            <p class="text-[14px] leading-[28.52px] text-[#403D3D] font-normal">۰۲۱۸۸۹۱۸۶۷۸-۰۲</p>
          </div>
          <div class="grid grid-cols-2">
            <p class="text-[16px] leading-[31.25px] text-primary-500 font-semibold">
              پست الکترونیکی:
            </p>
            <p class="text-[14px] leading-[28.52px] text-[#403D3D] font-normal">info@sant.ir</p>
          </div>
        </div>
      </div>

      <div class="col-span-2 md:col-span-1 order-first md:order-last">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d207344.80062931214!2d51.18284926061421!3d35.70746141773324!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3f8e00491ff3dcd9%3A0xf0b3697c567024bc!2sTehran%2C%20Tehran%20Province%2C%20Iran!5e0!3m2!1sen!2s!4v1692271901729!5m2!1sen!2s"
          class="w-full h-full aspect-square md:aspect-auto pb-[50px] md:pb-0"
          style="border: 0"
          allow="fullscreen="
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </div>
    </div>
  </section>
  <!-- Contact Detail:End -->

  <!-- Contact Form:Begin -->
  <section class="max-w-[1113px] mx-auto mt-[56px] mb-[120px] px-[40px] md:px-0">
    <div class="flex flex-col justify-center items-start">
      <h3 class="text-primary-500 text-[24px] leading-[37.5px] font-bold mb-[12px]">ارسال پیام</h3>
      <p class="text-secondary-500 text-[16px] leading-[29.64px] font-normal mb-[34px]">
        لطفا اطمینان حاصل نمائید تمامی موارد ستاره دار جهت ارسال پیام تکمیل شوند.
      </p>

      <form class="flex flex-col items-start w-full gap-[24px]">
        <div
          class="flex items-center justify-between w-full md:w-1/2 gap-x-[50px] gap-y-[8px] flex-col md:flex-row"
        >
          <label class="w-full text-[16px] leading-[25px] font-medium text-[#403D3D]"
            >نوع فعالیت: <span class="text-secondary-500">*</span></label
          >

          <select
            name="work_type"
            id="work_type"
            class="w-full rounded-[16px] border-[1px] border-[#8B8B8B] px-[16px] py-[8px] text-[14px] leading-[28.52px]"
          >
            <option disabled selected>نوع فعالیت خود را انتخاب کنید</option>
            <option>انتخاب اول</option>
            <option>انتخاب دوم</option>
          </select>
        </div>

        <div
          class="flex items-center justify-between w-full md:w-1/2 gap-x-[50px] gap-y-[8px] flex-col md:flex-row"
        >
          <label class="w-full text-[16px] leading-[25px] font-medium text-[#403D3D]"
            >نام و نام خانوادگی: <span class="text-secondary-500">*</span></label
          >

          <input
            type="text"
            name="work_type"
            id="work_type"
            placeholder="نام کامل خود را وارد کنید"
            class="w-full rounded-[16px] border-[1px] border-[#8B8B8B] px-[16px] py-[8px] text-[14px] leading-[28.52px]"
          />
        </div>

        <div
          class="flex items-center justify-between w-full md:w-1/2 gap-x-[50px] gap-y-[8px] flex-col md:flex-row"
        >
          <label class="w-full text-[16px] leading-[25px] font-medium text-[#403D3D]">ایمیل:</label>

          <input
            type="text"
            name="work_type"
            id="work_type"
            placeholder="Email@gmail.com"
            class="w-full rounded-[16px] border-[1px] border-[#8B8B8B] px-[16px] py-[8px] text-[14px] leading-[28.52px]"
          />
        </div>

        <div
          class="flex items-center justify-between w-full md:w-1/2 gap-x-[50px] gap-y-[8px] flex-col md:flex-row"
        >
          <label class="w-full text-[16px] leading-[25px] font-medium text-[#403D3D]"
            >شماره همراه: <span class="text-secondary-500">*</span></label
          >

          <input
            type="text"
            name="work_type"
            id="work_type"
            placeholder="912*******"
            dir="ltr"
            class="w-full rounded-[16px] border-[1px] border-[#8B8B8B] px-[16px] py-[8px] text-[14px] leading-[28.52px]"
          />
        </div>

        <div
          class="flex items-center justify-between w-full md:w-1/2 gap-x-[50px] gap-y-[8px] flex-col md:flex-row"
        >
          <label class="w-full text-[16px] leading-[25px] font-medium text-[#403D3D]">استان:</label>

          <input
            type="text"
            name="work_type"
            id="work_type"
            placeholder="تهران"
            class="w-full rounded-[16px] border-[1px] border-[#8B8B8B] px-[16px] py-[8px] text-[14px] leading-[28.52px]"
          />
        </div>

        <div
          class="flex items-center justify-between w-full md:w-1/2 gap-x-[50px] gap-y-[8px] flex-col md:flex-row mb-[20px]"
        >
          <label class="w-full text-[16px] leading-[25px] font-medium text-[#403D3D]">موضوع:</label>

          <input
            type="text"
            name="work_type"
            id="work_type"
            placeholder="شوینده‌های صنعتی"
            class="w-full rounded-[16px] border-[1px] border-[#8B8B8B] px-[16px] py-[8px] text-[14px] leading-[28.52px]"
          />
        </div>

        <div class="flex flex-col items-center justify-between w-full">
          <label class="w-full text-[16px] leading-[25px] font-medium text-[#403D3D] mb-[21px]">
            درخواست<span class="text-secondary-500">*</span>
          </label>

          <!-- <textarea id="editor"
                           class="w-full rounded-[16px] border-[1px] border-[#8B8B8B] px-[16px] py-[8px] text-[14px] leading-[28.52px]">
   
                       </textarea> -->
          <div id="editor—wrapper" class="w-full border-[1px] border-[#8B8B8B]">
            <div id="toolbar-container"><!-- toolbar --></div>
            <div id="editor-container"><!-- editor --></div>
          </div>
        </div>

        <div class="w-full flex items-center justify-end">
          <a
            class="px-[20px] py-[8px] text-white text-[16px] leading-[31px] font-semibold bg-santGreen rounded-[16px] inline-flex items-center justify-center"
          >
            ارسال پیام

            <ion-icon name="chevron-forward-outline" class="p-[8px] mr-[8px]"></ion-icon>
          </a>
        </div>
      </form>
    </div>
  </section>
  <!-- Contact Form:End -->
</template>
