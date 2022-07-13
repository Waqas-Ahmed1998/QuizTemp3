<template>
  <div v-if="show"  @click.self="closePopup()" class="tw-min-h-screen tw-bg-black/80 tw-fixed tw-top-0 tw-z-[10] tw-w-full tw-px-2 md:tw-px-0 ">

<!-- popup  -->
    <div :class="show && ''" class=" tw-bg-white tw-flex tw-flex-col tw-items-center tw-justify-center tw-w-[98%] md:tw-max-w-[720px] tw-absolute tw-top-[50%] tw-left-[50%] tw-translate-x-[-50%] tw-rounded-[10px] tw-bg-white  md:tw-px-[35px] min-h-[400px] tw-pt-[25px] tw-pb-[25px] tw-border-2 tw-border-[#704EDF] tw-translate-y-[-50%] tw-shrink-0 tw-px-2  ">

      <div class=" tw-flex tw-flex-col tw-items-center tw-justify-center">

        <h2 class="tw-text-black tw-text-[24px] tw-leading-[24px] md:tw-text-5xl tw-text-[#2f2f2f] tw-font-bold tw-text-center tw-mb-2 md:tw-mb-3">Where Would You Like Us To Send Your Free Download?</h2>

        <h2 class="tw-text-black tw-text-[18px] tw-leading-[24px] md:tw-text-3xl tw-text-[#2f2f2f] tw-font-medium tw-text-center tw-mb-4 md:tw-mb-6">This Is Sub Headline Below Headline</h2>


      <form action="" class="tw-flex tw-flex-col tw-justify-center  tw-mb-2 tw-w-full">
            <div class="tw-space-y-3 ">

       <input type="text" placeholder="Enter Your First Name..." class=" tw-border tw-border-[rgba(0,0,0,0.2)] focus:tw-outline-none   tw-w-full tw-rounded-[5px] tw-bg-[#F1F1F1]  text-black tw-px-[18px] tw-py-3  tw-text-[17px] md:tw-text-[24px] ">

       <input type="text" placeholder="Enter Your Best Email Address..." class=" tw-border tw-border-[rgba(0,0,0,0.2)] focus:tw-outline-none   tw-w-full tw-rounded-[5px] tw-bg-[#F1F1F1]  text-black tw-px-[18px] tw-py-3  tw-text-[17px] md:tw-text-[24px] ">

       <input type="text" placeholder="Enter Your Main Phone Number..." class=" tw-border tw-border-[rgba(0,0,0,0.2)] focus:tw-outline-none   tw-w-full tw-rounded-[5px] tw-bg-[#F1F1F1]  text-black tw-px-[18px] tw-py-3  tw-text-[17px] md:tw-text-[24px] ">




          </div>
            <button

              class="tw-mx-auto tw-cursor-pointer tw-bg-[#6438F8] hover:tw-bg-[#704edf]  tw-text-white tw-border-8 tw-border-transparent  tw-font-bold   hover:tw-animate-none  tw-py-2 md:tw-py-4 md:tw-px-4 md:tw-text-4xl tw-w-full md:tw-w-fit tw-flex  tw-space-x-2 md:tw-space-x-4  tw-justify-center tw-items-center tw-transition-all tw-ease-in-out tw-text-lg tw-rounded-full tw-mt-5 ">

            <span>DOWNLOAD NOW</span>

            </button>
</form>
<div id="disclaimer" class="">

  <p class="tw-space-x-2 tw-text-sm tw-text-center tw-w-fit tw-text-[#2f2f2f] ">  <span class="tw-relative tw-top-[2px] material-icons tw-text-xs md:tw-text-sm">
lock
</span> By clicking the button above you agree to receive email & txt msg marketing material we think you'll love. Opt-out anytime. Msg & data rates may apply.</p>
</div>
</div>
    </div>

  </div>
</template>

<script>



export default {
  name:'Popup1',

props:{
  show:Boolean,
},
data() {
  return {
    close:false,
  }
},

methods: {
  closePopup(){
    this.$emit('close')
  }
}
}
</script>

<!-- @click.self="close=!close" -->