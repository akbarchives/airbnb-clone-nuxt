<template>
  <nav class="select-none border-b-2 bg-white">
    <div class="mx-auto max-w-screen-2xl">
      <div class="h-20 px-6 sm:px-8">
        <!-- for Mobile Screen -->
        <div
          class="flex w-full flex-row items-center justify-between self-end sm:hidden"
        >
          <swiper
            :style="{
              '--swiper-button-next': '#00ff00',
              '--swiper-pagination-color': '#fff',
            }"
            :slidesPerView="6"
            :spaceBetween="30"
            :navigation="true"
            :modules="modules"
            class="mySwiper flex h-20 basis-auto flex-row items-end"
          >
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <NuxtLink to="/products">
                <img
                  class="mx-auto h-8 w-8"
                  src="~/assets/img/icon-category/room.png"
                  alt=""
                />
                <p class="py-1 text-sm font-medium">Products</p>
              </NuxtLink>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/room.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Rooms</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Arctic.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Arctic</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/beach.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Beach</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Golfing.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Golfing</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Hanoks.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Hanoks</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Islands.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Islands</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Tropical.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Tropical</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Camping.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Camping</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Lakefront.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Lakefront</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Boats.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Boats</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Design.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Designs</p> </swiper-slide
            ><swiper-slide
              class="flex min-w-fit flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Vineyards.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Vineyards</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Yurts.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Yurts</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Tiny-Homes.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Tiny Homes</p>
            </swiper-slide>
          </swiper>
          <ButtonFilter />
        </div>
        <!-- for MD screen -->
        <div
          class="hidden w-full flex-row items-center justify-between self-end sm:flex md:hidden"
        >
          <swiper
            :slidesPerView="6"
            :spaceBetween="30"
            :navigation="true"
            :modules="modules"
            class="mySwiper flex h-20 basis-auto flex-row items-end"
          >
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <NuxtLink to="/products">
                <img
                  class="mx-auto h-8 w-8"
                  src="~/assets/img/icon-category/room.png"
                  alt=""
                />
                <p class="py-1 text-sm font-medium">Products</p>
              </NuxtLink>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/room.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Rooms</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Arctic.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Arctic</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/beach.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Beach</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Golfing.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Golfing</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Hanoks.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Hanoks</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Islands.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Islands</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Tropical.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Tropical</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Camping.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Camping</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Lakefront.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Lakefront</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Boats.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Boats</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Design.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Designs</p> </swiper-slide
            ><swiper-slide
              class="flex min-w-fit flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Vineyards.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Vineyards</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Yurts.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Yurts</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Tiny-Homes.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Tiny Homes</p>
            </swiper-slide>
          </swiper>
          <ButtonFilter />
        </div>
        <!-- for MD screen -->
        <div
          class="hidden w-full flex-row items-center justify-between self-end md:flex lg:hidden"
        >
          <swiper
            :slidesPerView="8"
            :spaceBetween="30"
            :navigation="true"
            :modules="modules"
            class="mySwiper flex h-20 basis-auto flex-row items-end"
          >
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <NuxtLink to="/products">
                <img
                  class="mx-auto h-8 w-8"
                  src="~/assets/img/icon-category/room.png"
                  alt=""
                />
                <p class="py-1 text-sm font-medium">Products</p>
              </NuxtLink>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/room.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Rooms</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Arctic.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Arctic</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/beach.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Beach</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Golfing.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Golfing</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Hanoks.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Hanoks</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Islands.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Islands</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Tropical.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Tropical</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Camping.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Camping</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Lakefront.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Lakefront</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Boats.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Boats</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Design.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Designs</p> </swiper-slide
            ><swiper-slide
              class="flex min-w-fit flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Vineyards.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Vineyards</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Yurts.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Yurts</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Tiny-Homes.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Tiny Homes</p>
            </swiper-slide>
          </swiper>
          <ButtonFilter />
        </div>
        <!-- for LG screen -->
        <div
          class="hidden w-full flex-row items-center justify-between self-end lg:flex"
        >
          <swiper
            :slidesPerView="12"
            :spaceBetween="30"
            :navigation="true"
            :modules="modules"
            class="mySwiper flex h-20 basis-auto flex-row items-end"
          >
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <NuxtLink to="/products">
                <img
                  class="mx-auto h-8 w-8"
                  src="~/assets/img/icon-category/room.png"
                  alt=""
                />
                <p class="py-1 text-sm font-medium">Products</p>
              </NuxtLink>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/room.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Rooms</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Arctic.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Arctic</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/beach.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Beach</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Golfing.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Golfing</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Hanoks.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Hanoks</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Islands.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Islands</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Tropical.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Tropical</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Camping.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Camping</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Lakefront.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Lakefront</p> </swiper-slide
            ><swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Boats.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Boats</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Design.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Designs</p> </swiper-slide
            ><swiper-slide
              class="flex min-w-fit flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Vineyards.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Vineyards</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Yurts.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Yurts</p>
            </swiper-slide>
            <swiper-slide
              class="flex flex-col justify-center border-b-[3px] border-transparent pt-4 text-center opacity-70 duration-200 hover:border-b-[3px] hover:border-black hover:opacity-100 hover:duration-200"
            >
              <img
                class="mx-auto h-8 w-8"
                src="~/assets/img/icon-category/Tiny-Homes.png"
                alt=""
              />
              <p class="py-1 text-sm font-medium">Tiny Homes</p>
            </swiper-slide>
          </swiper>
          <ButtonFilter />
        </div>
      </div>
    </div>
  </nav>
</template>

<style>
nav {
  z-index: 999;
}
</style>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/navigation';

// import required modules
import { Navigation } from 'swiper';

export default {
  components: {
    Swiper,
    SwiperSlide,
  },

  props: {
    title: String,
    rating: Number,
    category: String,
    description: String,
    brand: String,
    image: String,
    price: Number,
    thumbnail: String,
    img: String,
    img1: String,
    img2: String,
    img3: String,
  },

  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>

<!-- <script setup>
import { AdjustmentsHorizontalIcon } from '@heroicons/vue/24/solid';
</script> -->
<style>
.swiper-button-disabled {
  display: none;
}
</style>
