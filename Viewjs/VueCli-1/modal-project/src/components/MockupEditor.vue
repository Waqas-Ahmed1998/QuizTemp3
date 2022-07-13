<template>
  <div class="relative tw-min-h-screen tw-bg-white ">
<!-- Editor  -->

<div class=" tw-p-4 tw-absolute tw-z-[20] tw-bottom-2 tw-right-2 tw-w-[350px] tw-bg-blue-400 tw-min-h-[400px] tw-rounded-md tw-shadow-[0_0_3px_black]">

<form @submit.prevent action="">

<div>
  <label for="line-height" class="tw-block tw-mb-2 tw-text-sm tw-font-medium tw-text-gray-900 tw-dark:text-gray-400">Select line height</label>
<select v-model="lineHeight" id="line-height" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 leadingblock w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500 tw-py-1 tw-px-1 tw-rounded-sm tw-w-full">
  <option :value='lineHeight' selected>{{lineHeight}}px
    </option>
  <option value=12>12px</option>
  <option value=14>14px</option>
  <option value=16>16px</option>
  <option value=18>18px</option>
  <option value=20>20px</option>
  <option value=30>30px</option>
  <option value=32>32px</option>
  <option value=34>34px</option>

</select>

</div>
<div>
  <label for="space-bottom" class="tw-block tw-mb-2 tw-text-sm tw-font-medium tw-text-gray-900 tw-dark:text-gray-400">Space Bottom</label>
<select v-model="spaceBottom" id="space-bottom" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 leadingblock w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500 tw-py-1 tw-px-1 tw-rounded-sm tw-w-full">
  <option value=31 selected>31px
    </option>
  <option value=12>12px</option>
  <option value=14>14px</option>
  <option value=16>16px</option>
  <option value=18>18px</option>
  <option value=20>20px</option>
  <option value=30>30px</option>
  <option value=32>32px</option>
  <option value=34>34px</option>
</select>

</div>
<div>
  <label for="space-top" class="tw-block tw-mb-2 tw-text-sm tw-font-medium tw-text-gray-900 tw-dark:text-gray-400">Space Top</label>
<select v-model="spaceTop" id="space-top" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 leadingblock w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500 tw-py-1 tw-px-1 tw-rounded-sm tw-w-full">
  <option value=31 selected>31px
    </option>
  <option value=12>12px</option>
  <option value=14>14px</option>
  <option value=16>16px</option>
  <option value=18>18px</option>
  <option value=20>20px</option>
  <option value=30>30px</option>
  <option value=32>32px</option>
  <option value=34>34px</option>
</select>

</div>
<div>
  <label for="font-size" class="tw-block tw-mb-2 tw-text-sm tw-font-medium tw-text-gray-900 tw-dark:text-gray-400">Font Size</label>
<select v-model="fontSize" id="font-size" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 leadingblock w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500 tw-py-1 tw-px-1 tw-rounded-sm tw-w-full">
  <option value=31 selected>31px
    </option>
  <option value=12>12px</option>
  <option value=14>14px</option>
  <option value=16>16px</option>
  <option value=18>18px</option>
  <option value=20>20px</option>
  <option value=30>30px</option>
  <option value=32>32px</option>
  <option value=34>34px</option>
</select>>

</div>

<button @click="save()"></button>
</form>

</div>

  <div class="tw-relative  tw-mx-auto  tw-items-center  tw-overflow-x-hidden ">


    <div
      class="tw-mx-auto tw-max-w-[1170px]   tw-rounded-sm md:tw-mt-14   tw-relative tw-z-10    tw-items-center tw-justify-center    ">


      <div
        class=" md:tw-p-0 lg:tw-px-10 tw-bg-transparent tw-w-full tw-px-2 tw-flex tw-flex-col tw-items-center tw-pt-5 md:tw-py-0 tw-relative tw-z-[3] md:tw-top-auto tw-mx-auto  tw-text-center tw-space-y-2 md:tw-space-y-2 ">

        <p
          class="  tw-text-center   tw-font-bold tw-text-[26px] tw-leading-[26px] md:tw-text-[40px] md:tw-leading-[40px] tw-text-[#2d2d2d]   w-fit md:tw-pb-0 md:tw-pt-0 tw-shadow-green-600 tw-drop-shadow-2xl [text-shadow:0px_0px_10px_#ff0000]">
          Download Our Grow Your Group Guide Below Now</p>
        <h2


          :class="`tw-text-[${fontSize}px] tw-leading-[${lineHeight}px]  md:tw-text-[${fontSize}px] md:tw-leading-[${fontSize}px]  tw-text-center   tw-font-bold md:tw-pb-0 tw-text-[#2d2d2d] md:tw-pb-[${spaceBottom}px]`"

          >

          The Verry Simple Tool That Allow You to Create High Converting Quizzes, Survey And Applications...

        </h2>

        <p
          class="  tw-text-[21px] tw-leading-[21px] md:tw-text-[36px] md:tw-leading-[36px] tw-text-[#2d2d2d] md:tw-pt-0  md:tw-pb-0 ">
          ... And the ability to sort, sift and separate at the same time!</p>

        <div class="tw-w-full">
          <form action=""
            class="tw-flex tw-flex-col md:tw-px-5 tw-justify-center tw-w-full tw-px-1 md:tw-w-[95%] tw-space-y-3  md:tw-space-y-6  tw-rounded-md  tw-mb-2 tw-mt-4 md:tw-mt-8  tw-items-center ">



            <input type="email" placeholder="Your Email Address Here ..."
              class="tw-outline-none tw-border  tw-rounded-md tw-w-full lg:tw-w-full  tw-shadow-sm tw-text-black  tw-text-sm md:tw-text-base  tw-px-4 tw-py-3 ">



            <!-- <div class=" tw-w-full md:tw-w-full "> -->

            <button
              class="tw-cursor-pointer  tw-text-white tw-border tw-border-b-2 tw-border-b-[rgba(0,0,0,0.2)] tw-font-semibold md:tw-font-bold   hover:tw-animate-none  tw-py-[10px] md:tw-py-6 tw-px-[30px] tw-text-[28px] tw-leading-[28px] md:tw-text-[70px] md:tw-leading-[70px] tw-w-full  md:tw-w-fit tw-flex btn tw-space-x-2 md:tw-space-x-4  tw-justify-center tw-items-center tw-transition-all sm:group-hover:tw--translate-y-3 sm:group-hover:tw-px-10  tw-ease-in-out  tw-rounded-md tw-bg-[#67BA39] md:hover:tw-bg-[#63d029] t">

              <p class="">Download Now!</p>

            </button>


            <!-- </div> -->


            <p
              class=" tw-align-baseline tw-text-xs md:tw-text-sm tw-text-center tw-font-medium disclaimer tw-text-[black] ">
              We respect
              your
              privacy,
              Your
              email
              address will
              never be
              shared or sold</p>


          </form>
        </div>
      </div>

    </div>

  </div>

</div>
</template>

<script>
export default {
name:'MockupEditor',
data(){
  return {
    lineHeight:40,
    spaceBottom:1,
    spaceTop:1,
    fontSize:40,
    large:1
  }
}
}
</script>

<style>

</style>