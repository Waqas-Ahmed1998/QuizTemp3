<template>
<!-- parent container  -->

<div class="tw-min-h-screen tw-bg-[#414EC5] tw-flex tw-flex-col ">


<header class="tw-py-4 tw-px-2 md:tw-px-8 lg:tw-px-12 md:tw-py-6  tw-space-y-3 md:space-y-0 ">

  <div class="  tw-flex tw-w-full  tw-items-center tw-justify-between  xl:tw-justify-center tw-items-center   ">

<!-- arrow icon previous only be shown in mobile view   -->
   <span @click="previousQuestion" class=" material-icons xl:tw-hidden tw-inline-block tw-text-white tw-cursor-pointer">
    west
  </span>

<!-- this logo image will be shown to both mobile and desktop  -->
    <img src="../assets/Quizforma-logo.svg" alt="" class="tw-w-32  md:tw-w-auto ">

<!-- Nubmer counter only be shown in mobile view   -->
<span class=" tw-text-white xl:tw-hidden">2 / 9 </span>

</div>
<!-- progress bar for mobile  -->
  <div class="tw-block xl:tw-hidden tw-w-full  tw-h-1 tw-bg-white tw-rounded-r-md md:tw-w-[90%] tw-mx-auto">
        <div :class="` tw-w-[15%] tw-h-1 tw-bg-blue-600 tw-rounded-r-md`"></div>
   </div>

</header>

<!-- main screen container  -->

  <div id="popup" class=" md:tw-rounded-md tw-w-full md:tw-max-w-[600px] lg:tw-max-w-[700px] xl:tw-max-w-[1100px]  tw-top-0  tw-ease-in-out   md:tw-min-h-[695px] tw-flex tw-flex-col  tw-text-center  tw-bg-white   tw-min-h-[70vh]  tw-mx-auto montserat tw-relative ">

    <!-- top content it will be hidden on mobile view   -->

    <div class="tw-hidden  xl:tw-flex tw-relative tw-justify-center md:tw-justify-between tw-items-center  tw-p-6 ">
      <h2 class="tw-font-semibold md:tw-text-[20px] tw-text-[#414EC5] "> 3 out of 9</h2>

      <div class="md:tw-space-x-3  md:tw-px-0 tw-flex tw-w-full md:tw-w-fit tw-absolute md:tw-relative tw-justify-between md:tw-justify-start">
        <!-- left arrow  -->
        <i
         @click="previousQuestion" class="tw-flex md:tw-scale-[1.2] lg:hover:tw-border-[#414EC5] lg:hover:tw-text-[#4b57c2]  tw-transition-colors tw-ease-out tw-items-center tw-rounded-full tw-border-[2px] tw-text-[#C6C6C6] tw-border-[#ECECEC] tw-cursor-pointer "><svg
            class="" xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px"
            fill="currentColor">
            <path d="M0 0h24v24H0V0z" fill="none" />
            <path
              d="M14.71 6.71c-.39-.39-1.02-.39-1.41 0L8.71 11.3c-.39.39-.39 1.02 0 1.41l4.59 4.59c.39.39 1.02.39 1.41 0 .39-.39.39-1.02 0-1.41L10.83 12l3.88-3.88c.39-.39.38-1.03 0-1.41z" />
          </svg></i>

        <!-- right arrow  -->
        <i
          @click="nextQuestion" class="  tw-flex md:tw-scale-[1.2] lg:hover:tw-border-[#414EC5] lg:hover:tw-text-[#4b57c2] tw-transition-colors tw-ease-out tw-items-center tw-text-[#C6C6C6] tw-rounded-full tw-border-[2px] tw-border-[#ECECEC] tw-cursor-pointer "><svg
            xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor">
            <path d="M0 0h24v24H0V0z" fill="none" />
            <path
              d="M9.31 6.71c-.39.39-.39 1.02 0 1.41L13.19 12l-3.88 3.88c-.39.39-.39 1.02 0 1.41.39.39 1.02.39 1.41 0l4.59-4.59c.39-.39.39-1.02 0-1.41L10.72 6.7c-.38-.38-1.02-.38-1.41.01z" />
          </svg></i>
      </div>
      <!-- progress bar  -->
      <div class="  tw-w-full tw-bottom-0 tw-left-0 tw-absolute tw-h-1 tw-bg-[#ECECEC]">
        <div :class="`!tw-w-[15%] tw-h-1 tw-bg-[#414EC5]`"></div>
      </div>
    </div>

    <!-- middle content  contains inputs , question  and image -->

    <div class="tw-mt-[50px] md:tw-mt-[70px] xl:tw-mt-[50px] tw-relative tw-px-2 tw-pb-4   ">

      <div class="tw-flex tw-flex-col tw-items-center tw-self-start ">

        <img src="../assets/Name_Icon.svg" alt="" class="tw-my-2">

        <!-- question part  -->

        <h2 class="md:tw-text-base tw-text-[#414EC5]">Student Name</h2>

<!-- short desc part  -->

   <span class="tw-text-sm tw-my-3">Type a description</span>

      <!-- main input container  -->
   <div class=" tw-mt-6 md:tw-px-6 lg:tw-px-10 xl:tw-px-0 tw-text-xs md:tw-text-base tw-w-full xl:tw-max-w-[575px]   ">

      <!-- when name information required  -->

        <div v-if="currentScreen==1" class="tw-space-y-3 ">
          <input type="text" placeholder="First Name"
            class="tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]  tw-min-h-[50px]">
          <input type="text" placeholder="Middle Name"
            class="tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]  tw-min-h-[50px]">
          <input type="text" placeholder="Last Name"
            class=" tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]   tw-min-h-[50px]">
       </div>


<!-- when Address information required  -->

   <div v-if="currentScreen==2" class="tw-space-y-3">

        <div class="tw-flex tw-gap-2 ">
            <input type="text" placeholder="Street Address"
             class=" tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]   tw-min-h-[50px]">
            <input type="text" placeholder="Street Address Line 2"
         class=" tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]   tw-min-h-[50px]">
        </div>

          <input type="text" placeholder="City"
           class=" tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]   tw-min-h-[50px]">

       <div class="tw-w-full tw-flex tw-gap-2">
            <input type="text" placeholder="State / Province"
         class=" tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]   tw-min-h-[50px]">
            <input type="text" placeholder="Postal / Zip Code"
         class=" tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]   tw-min-h-[50px]">
       </div>
    </div>


<!-- when email information required  -->
   <div v-if="currentScreen==3" class="tw-space-y-3">

            <input type="email" placeholder="example@mail.com"
             class=" tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]   tw-min-h-[50px]">

   </div>

   <!-- when phone number information required  -->
   <div v-if="currentScreen==4" class="tw-space-y-3">

            <input type="number" placeholder="(XXX)(XXXXXXX)"
             class=" tw-placeholder-black  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5]   tw-min-h-[50px]">

   </div>

   <!-- when dropdown information required  -->

           <div v-if="currentScreen==5" class=" tw-relative">
            <select
              class="tw-block tw-appearance-none tw-w-full tw-bg-white tw-border tw-border-[#414EC5] tw-min-h-[50px] tw-px-4 tw-pr-8 tw-rounded tw-leading-tight focus:tw-outline-none   tw-text-black"
              id="grid-state ">

              <option value="" disabled selected hidden>Please Select</option>
              <option>Option 1</option>
              <option>Option 2</option>
            </select>
            <div class="tw-pointer-events-none tw-absolute tw-inset-y-0 tw-right-0 tw-flex tw-items-center tw-px-2 tw-text-[#414EC5]">
              <svg class="tw-fill-current tw-h-4 tw-w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
                <path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z" />
              </svg>
            </div>
          </div>

<!--when multiple choice options information required (Power Type) -->

    <div v-if="currentScreen==6" class="tw-w-full">

              <div class="tw-flex tw-flex-col tw-space-y-3">

            <!-- option-1 -->

            <div @click="option1Selected=!option1Selected" id="popup-8-option-1" :class="`${option1Selected && 'tw-bg-[#414EC5] tw-text-white'} tw-w-full tw-rounded-[60px] tw-border tw-border-[#E5E5E5]  tw-transition-colors tw-ease-out lg:hover:tw-border-[#414EC5] tw-bg-white md:tw-min-h-[43px] tw-cursor-pointer  tw-flex tw-items-center tw-pl-2 tw-pr-2 tw-space-x-3  tw-py-2 md:tw-py-0 tw-relative `">

              <!-- option  -->

              <span class="tw-rounded-full tw-flex tw-justify-center tw-items-center tw-text-center tw-w-[22px] tw-min-h-[22px] md:tw-w-[27px] md:tw-h-[27px] tw-bg-[#F6F6F6] tw-text-lg  tw-font-medium tw-text-[#005C7D] ">

                <span id="popup-8-choice-1"
                  ref="option1" :class="`${!option1Selected && 'tw-hidden'}  tw-w-[60%] tw-h-[60%] tw-rounded-full tw-bg-[#717DEE] tw-shadow-[1px_2px_3px_rgba(0,0,0,0.14)]`"></span>

                  </span>

              <!-- option content  -->

              <span class="tw-text-sm md:tw-text-base  option-1-text-color  ">Choice A</span>

              <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" tw-absolute tw-right-0 tw-appearance-none">

            </div>

            <!-- option-2 -->

            <div @click="option2Selected=!option2Selected" id="popup-8-option-1" :class="`${option2Selected && 'tw-bg-[#414EC5] tw-text-white'} tw-w-full tw-rounded-[60px] tw-border tw-border-[#E5E5E5]  tw-transition-colors tw-ease-out lg:hover:tw-border-[#414EC5] tw-bg-white md:tw-min-h-[43px] tw-cursor-pointer  tw-flex tw-items-center tw-pl-2 tw-pr-2 tw-space-x-3  tw-py-2 md:tw-py-0 tw-relative `">

              <!-- option  -->

              <span class="tw-rounded-full tw-flex tw-justify-center tw-items-center tw-text-center tw-w-[22px] tw-min-h-[22px] md:tw-w-[27px] md:tw-h-[27px] tw-bg-[#F6F6F6] tw-text-lg  tw-font-medium tw-text-[#005C7D] "><span id="popup-8-choice-1"
                 ref="option2"  :class="`${!option2Selected && 'tw-hidden'}  tw-w-[60%] tw-h-[60%] tw-rounded-full tw-bg-[#717DEE] tw-shadow-[1px_2px_3px_rgba(0,0,0,0.14)]`"></span></span>

              <!-- option content  -->

              <span class="tw-text-sm md:tw-text-base   option-1-text-color  ">Choice B</span>

              <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" tw-absolute tw-right-0 tw-appearance-none">

            </div>

   <!-- option-3 -->
              <div @click="option3Selected=!option3Selected" id="popup-8-option-1" :class="`${option3Selected && 'tw-bg-[#414EC5] tw-text-white'} tw-w-full tw-rounded-[60px] tw-border tw-border-[#E5E5E5]  tw-transition-colors tw-ease-out lg:hover:tw-border-[#414EC5] tw-bg-white md:tw-min-h-[43px] tw-cursor-pointer  tw-flex tw-items-center tw-pl-2 tw-pr-2 tw-space-x-3  tw-py-2 md:tw-py-0 tw-relative `">

              <!-- option  -->

              <span class="tw-rounded-full tw-flex tw-justify-center tw-items-center tw-text-center tw-w-[22px] tw-min-h-[22px] md:tw-w-[27px] md:tw-h-[27px] tw-bg-[#F6F6F6] tw-text-lg  tw-font-medium tw-text-[#005C7D] "><span id="popup-8-choice-1"
                ref="option3"  :class="`${!option3Selected && 'tw-hidden'} tw-w-[60%] tw-h-[60%] tw-rounded-full tw-bg-[#717DEE] tw-shadow-[1px_2px_3px_rgba(0,0,0,0.14)]`"></span></span>

              <!-- option content  -->

              <span class="tw-text-sm md:tw-text-base  option-1-text-color  ">Choice C</span>

              <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" tw-absolute tw-right-0 tw-appearance-none">

            </div>
   <!-- option-4 -->
              <div @click="option4Selected=!option4Selected" id="popup-8-option-1" :class="`${option4Selected && 'tw-bg-[#414EC5] tw-text-white'} tw-w-full tw-rounded-[60px] tw-border tw-border-[#E5E5E5]  tw-transition-colors tw-ease-out lg:hover:tw-border-[#414EC5] tw-bg-white md:tw-min-h-[43px] tw-cursor-pointer  tw-flex tw-items-center tw-pl-2 tw-pr-2 tw-space-x-3  tw-py-2 md:tw-py-0 tw-relative `">

              <!-- option  -->

              <span class="tw-rounded-full tw-flex tw-justify-center tw-items-center tw-text-center tw-w-[22px] tw-min-h-[22px] md:tw-w-[27px] md:tw-h-[27px] tw-bg-[#F6F6F6]  tw-text-lg  tw-font-medium tw-text-[#005C7D] ">

                <span id="popup-8-choice-1"
                ref="option4"  :class="`${!option4Selected && 'tw-hidden'} tw-bg-[#414EC5] tw-w-[60%] tw-h-[60%] tw-rounded-full tw-shadow-[1px_2px_3px_rgba(0,0,0,0.14)]`"></span>


                </span>

              <!-- option content  -->

              <span class="tw-text-sm md:tw-text-base  option-1-text-color  ">Choice D</span>

              <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" tw-absolute tw-right-0 tw-appearance-none">

            </div>

          </div>
    </div>

<!-- When yes or No information needed (Power Type)  -->

         <div v-if="currentScreen==7">
            <button class=" tw-w-fit tw-px-6 tw-py-2 md:tw-px-0 md:tw-py-0 border-[#414EC5] lg:hover:tw-bg-[#414EC5] md:tw-w-[160px] tw-border  md:tw-h-[60px] tw-rounded-lg tw-transition-colors tw-ease-in-out tw-bg-white tw-text-black  lg:hover:tw-text-white tw-text-base md:tw-text-xl tw-mx-2">Yes</button>

            <button class=" tw-w-fit tw-px-6 tw-py-2 md:tw-px-0 md:tw-py-0 border-[#414EC5] lg:hover:tw-bg-[#414EC5] md:tw-w-[160px] tw-border  md:tw-h-[60px] tw-rounded-lg tw-transition-colors tw-ease-in-out tw-bg-white tw-text-black  lg:hover:tw-text-white tw-text-base md:tw-text-xl tw-mx-2">No</button>
          </div>

 <!-- When detailed information needed (General Type long box)  -->

   <div v-if="currentScreen==8" class="tw-space-y-3">


        <textarea autofocus name="" id="" cols="30" rows="10" placeholder="Type a long description here....." class="tw-placeholder-black tw-py-2  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5] [resize:none] tw-min-h-[50px]"></textarea>

   </div>

      <!-- When short information needed (General Type short box)  -->

   <div v-if="currentScreen==9" class="tw-space-y-3">

      <textarea autofocus name="" id="" cols="30" rows="3" placeholder="Type a short description here....." class="tw-placeholder-black tw-py-2  tw-px-2 focus:tw-ring-0 focus:tw-outline-none tw-rounded-[6px] tw-w-full tw-border tw-border-[#414EC5] [resize:none] tw-min-h-[50px]"></textarea>

   </div>

  </div>


<!-- Button for next question  -->

            <button @click="nextQuestion" class=" tw-transition-colors tw-ease-in-out tw-border tw-border-[#414EC5] tw-rounded-xl xl:hover:tw-bg-[#414EC5] xl:hover:tw-text-white tw-px-4 tw-py-2 tw-mt-10 tw-tracking-wide md:tw-text-xl">Next</button>
  </div>

  </div>



  </div>

<footer class="tw-text-white tw-flex  tw-items-center tw-w-full tw-flex-col tw-py-5   xl:tw-py-8 tw-px-2 tw-space-y-2 tw-text-xs md:tw-text-sm tw-font-extralight">

  <p class=" popins ">Copyright © My Company. All Rights Reserved. </p>

  <p class=""><a href="">Terms of Service</a> | <a href="">Privacy Policy</a> | <a href="">Contact Us</a></p>


</footer>

  </div>

</template>

<script>
export default {
name:'QuizForma1',
data(){
  return {
currentScreen:1,
totelQuizScreens:9,
option1Selected:false,
option2Selected:false,
option3Selected:false,
option4Selected:false,

  }
},
methods:{
  nextQuestion(){
    if(this.currentScreen < this.totelQuizScreens)  this.currentScreen++
  },
  previousQuestion(){

    if(this.currentScreen!=1)  this.currentScreen--

  },

  selectMultipleChoiceOption(){

  }
}
}
</script>

<style>

</style>