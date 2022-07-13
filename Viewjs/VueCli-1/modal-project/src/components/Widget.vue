<template>
<!-- for background  -->
<div  class="tw-bg-black/80 tw-min-h-screen">
<!-- main widget div  -->

  <div ref="widget" class="   tw-fixed tw-bottom-0 md:tw-left-2 md:tw-space-x-4 tw-flex tw-flex-row  bg-transparent tw-text-black tw-w-full sm:tw-w-[480px] ">
    <div class="tw-min-h-[90px] tw-w-[100px]">
      <img src="../assets/widgetLogo.jpg" alt="" class="md:tw-rounded-xl tw-w-full tw-h-full  tw-object-cover ">
    </div>

<!-- content parent div making pointer icon correct to its position  -->
    <div class="tw-relative tw-w-full   ">

<!-- pointer icon -->

    <i class="tw-hidden md:tw-inline-block tw-absolute tw-z-[0]  -tw-left-[7px] tw-top-3 tw-rotate-45 tw-border-[10px] tw-border-white "></i>

<!-- content div  -->
    <div class="tw-relative tw-px-2 tw-py-2 md:tw-p-3 tw-z-[1] tw-bg-white md:tw-rounded-md tw-w-full tw-h-full   ">

<!-- top content div contains icons and top title -->
    <div class="tw-flex tw-justify-between tw-items-center tw-text-stone-500 tw-text-xs ">
      <p class="tw-w-fit  tw-text-xs md:text-sm ">Clark Kent</p>

<!-- icons div  -->
    <div class=" tw-space-x-1 ">

      <span class="material-icons  tw-text-xs tw-cursor-pointer  ">
        help
        </span>

      <span  @click="closeWidget" class="material-icons  tw-text-xs tw-cursor-pointer">
          close
          </span>
    </div>

</div>

<!-- inner content  -->
  <div  class="tw-flex tw-w-full  tw-items-center tw-justify-between tw-text-black tw-pt-2 tw-space-x-1  ">

    <p class="tw-text-sm md:tw-text-base tw-font-light">Sign up and customize the CTA!</p>

    <button class=" tw-text-sm md:tw-text-base tw-px-2 tw-py-2 md:tw-px-3 md:tw-py-2 tw-bg-blue-400 tw-text-white tw-text-base tw-rounded-md tw-tracking-wide">Click Here</button>
  </div>

    </div>
  </div>

  </div>
</div>
</template>

<script>
export default {
name:'Widget',
data() {
  return {
    hello:true
  }
},
  methods: {
    closeWidget(){
this.$refs.widget.classList.add('tw-hidden')
    }
  }
}
</script>

<style>

</style>