<template>
          <section
          :class="!withVideo && 'tw-mx-auto'"
          class=" md:tw-px-[10px] tw-max-w-[96%]  ">

          <h2
            class="tw-tracking-wide tw-mb-6 tw-text-center bullet-heading tw-text-base md:tw-text-[28px] md:tw-leading-[1.3] tw-text-[#2f2f2f] tw-font-bold tw-text-white fonts-lato">
      in this training you will learn:</h2>


          <ul class="tw-flex tw-flex-col tw-space-y-3 fonts-raleway">
            <!-- *********bullet point content  -->
            <div class="tw-flex tw-space-x-3">
              <span class="material-icons tw-text-[#47A6EA] tw-mt-[3px]">
              check_circle
              </span>

              <p class="tw-inline-block tw-text-base md:tw-text-[20px] tw-text-[#f1f1f1] md:tw-leading-[29px]  ">
             The overlooked reasons why digital marketing usually ends up failing for many businesses and the exact steps to take so you can avoid these failures and actually use them to your advantage
              </p>
            </div>
            <div class="tw-flex tw-space-x-3">
              <span class="material-icons tw-text-[#47A6EA] tw-mt-[3px]">
              check_circle
              </span>

              <p class="tw-inline-block tw-text-base md:tw-text-[20px] tw-text-[#f1f1f1] md:tw-leading-[29px] ">
       What the real problem is for why digital marketing usually doesn't turn out as expected and why it isn't your fault!
              </p>
            </div>
            <div class="tw-flex tw-space-x-3 ">
              <span class="material-icons tw-text-[#47A6EA] tw-mt-[3px]">
              check_circle
              </span>

              <p class="tw-inline-block tw-text-base md:tw-text-[20px] tw-text-[#f1f1f1] md:tw-leading-[29px] ">
         My revolutionary but simple approach to stop any failing digital marketing strategy in its tracks and to start seeing growth QUICKER and EASIER.
              </p>
            </div>
            <div class="tw-flex tw-space-x-3">
              <span class="material-icons tw-text-[#47A6EA] tw-mt-[3px]">
              check_circle
              </span>

              <p class="tw-inline-block tw-text-base md:tw-text-[20px] tw-text-[#f1f1f1] md:tw-leading-[29px] ">
   The real digital marketing keys I've learned, tested, and currently use to help transform and grow thousands of other businesses digitally over 18+ years.
              </p>
            </div>

            <!-- <div class="tw-flex tw-space-x-4">
              <i class="tw-inline-block tw-mt-1 h-fit "> <svg xmlns="http://www.w3.org/2000/svg" class="tw-h-5 tw-w-5 tw-scale-[1.5] "
                  viewBox="0 0 20 20" fill="currentColor">
                  <path fill-rule="evenodd"
                    d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z"
                    clip-rule="evenodd" />
                </svg></i>

              <p class="tw-inline-block tw-text-base md:tw-text-lg tw-text-white"><span class="tw-font-bold tw-text-blue-500"> Bullet #1:</span>
                This would be a benefit or result for your 1st bullet. You want this to be about 2-3 lines. Make it
                exciting!
              </p>
            </div> -->

          </ul>

        </section>
</template>

<script>
export default {
name:'Bullets',
props:{
  withVideo:Boolean
}
}
</script>

<style>

</style>