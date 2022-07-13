<template>
<div class="min-h-screen bg-[#BBB6D9] flex flex-col">
<!-- bg-gradient-to-b from-blue-500  to-blue-400 -->
<header class="py-4 px-2 md:px-4 lg:px-6 xl:px-10  space-y-3 ">

  <div class="  flex w-full  items-center justify-between   ">

<!-- arrow icon previous only be shown in mobile view   -->

<svg @click="previousQuestion" class=" text-white cursor-pointer transition-colors ease-out xl:hover:text-[#261641]"  xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M9,19l1.41-1.41L5.83,13H22V11H5.83l4.59-4.59L9,5l-7,7L9,19z"/></svg>

<!-- this logo image will be shown to both mobile and desktop  -->
    <img src="../../assets/Quizforma-logo.svg" alt="" class="scale-[0.7] w-32   md:w-auto ">

<!-- Nubmer counter only be shown in mobile view   -->
    <span class=" text-white md:text-base lg:text-lg xl:text-xl "><span class="text-[#1E3253]">{{currentScreen}}</span> / {{totelQuizScreens}} </span>

</div>
<!-- progress bar  -->
  <div class="block  w-[90%]  h-1 bg-white rounded-r-md md:max-w-[480px] mx-auto">
        <div :class="` w-[15%] h-1 bg-[#1E3253] rounded-r-md`"></div>
   </div>

</header>

<!-- main content container  -->

 <section class=" w-full md:w-[480px] mx-auto py-4 px-2   ">
<!-- question and details  -->
    <div class="space-y-3 text-center">

   <h2 class="text-xl md:text-2xl text-[#261641] font-semibold">Tell Us About Your Name</h2>

   <p class="text-base md:text-xl text-[#261641]/90">Some description</p>


    </div>

    <!-- main container contain all inputs and screen related data  -->
   <main class="w-full my-6 min-h-[400px] ">

<!-- personal information  -->

      <section v-if="currentScreen==2"  class="space-y-3 ">



          <input type="text" placeholder="First Name"
            class="placeholder-black/80 text-[#261641] focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]   text-sm md:text-base bg-white shadow-[0_0_3px_white] border border-transparent focus:border-[#EBBC42]  px-2 md:px-4">

          <input type="text" placeholder="Middle Name"
            class="placeholder-black/80 text-[#261641]   focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]  text-sm md:text-base  shadow-[0_0_3px_white] bg-white border border-transparent focus:border-[#EBBC42] px-2 md:px-4">

          <input type="text" placeholder="Last Name"
            class="placeholder-black/80 text-[#261641]   focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]  text-sm md:text-base  shadow-[0_0_3px_white] bg-white border border-transparent focus:border-[#EBBC42] px-2  md:px-4 ">

        </section>

<!-- multiple options information  -->

        <section v-if="currentScreen==1" class="flex flex-col space-y-3">

            <!-- option-1 -->

            <div @click="option1Selected=!option1Selected" id="popup-8-option-1" :class="`${option1Selected && 'bg-[#928bc0b3] !text-white border-[#EBBC42]' } bg-white text-[#261641]/80 w-full rounded-[12px] transition-colors ease-out l md:min-h-[80px] cursor-pointer border border-transparent flex items-center  space-x-3  py-2 md:py-0 relative min-h-[50px] shadow-[0_0_3px_white]   px-2 md:px-4 font-semibold`">

              <!-- option  -->

              <!-- <span class="rounded-full flex justify-center items-center text-center w-[27px] min-h-[27px] md:w-[32px] md:h-[32px] bg-[#F6F6F6]  font-medium text-[#005C7D] ">

                <span id="popup-8-choice-1"
                  ref="option1" :class="`${!option1Selected && 'opacity-0 '} transition-opacity ease-in-out w-[17px] h-[17px]  md:w-[60%] md:h-[60%] rounded-full bg-white   shadow-[1px_2px_3px_rgba(0,0,0,0.14)]`"></span>

                  </span> -->

              <!-- option content  -->

                 <div class="flex justify-between w-full">
              <span class="text-sm md:text-base font-semibold ">Lorem ipsum dolor sit amet C </span>

              <!-- icon  -->
            <svg :class="`hidden text-[#EBBC42] transition-opacity ease-in-out opacity-0 ${option1Selected && 'opacity-100'} `" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M22,5.18L10.59,16.6l-4.24-4.24l1.41-1.41l2.83,2.83l10-10L22,5.18z M19.79,10.22C19.92,10.79,20,11.39,20,12 c0,4.42-3.58,8-8,8s-8-3.58-8-8c0-4.42,3.58-8,8-8c1.58,0,3.04,0.46,4.28,1.25l1.44-1.44C16.1,2.67,14.13,2,12,2C6.48,2,2,6.48,2,12 c0,5.52,4.48,10,10,10s10-4.48,10-10c0-1.19-0.22-2.33-0.6-3.39L19.79,10.22z"/></svg>

              </div>

              <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" absolute right-0 appearance-none">

            </div>

            <!-- option-2 -->

            <div @click="option2Selected=!option2Selected" id="popup-8-option-1" :class="`${option2Selected && 'bg-[#928bc0b3] !text-white border-[#EBBC42]' } bg-white text-[#261641]/80  w-full rounded-[12px] transition-colors ease-out  md:min-h-[80px] cursor-pointer border border-transparent flex items-center  space-x-3  py-2 md:py-0 relative min-h-[50px] shadow-[0_0_3px_white]   px-2 md:px-4 font-semibold`">

              <!-- option  -->

              <!-- <span class="rounded-full flex justify-center items-center text-center  w-[27px] min-h-[27px] md:w-[32px] md:h-[32px]  bg-[#F6F6F6]  font-medium text-[#005C7D] ">

                <span id="popup-8-choice-1"
                 ref="option2"  :class="`${!option2Selected && 'opacity-0 '} transition-opacity ease-in-out  w-[17px] h-[17px]  md:w-[60%] md:h-[60%]  rounded-full bg-white shadow-[1px_2px_3px_rgba(0,0,0,0.14)]`"></span>
                 </span> -->

              <!-- option content  -->

                <div class="flex justify-between w-full">
              <span class="text-sm md:text-base font-semibold ">Lorem ipsum dolor sit amet C </span>

              <!-- icon  -->
             <svg :class="`hidden text-[#EBBC42] transition-opacity ease-in-out opacity-0 ${option2Selected && 'opacity-100'} `" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M22,5.18L10.59,16.6l-4.24-4.24l1.41-1.41l2.83,2.83l10-10L22,5.18z M19.79,10.22C19.92,10.79,20,11.39,20,12 c0,4.42-3.58,8-8,8s-8-3.58-8-8c0-4.42,3.58-8,8-8c1.58,0,3.04,0.46,4.28,1.25l1.44-1.44C16.1,2.67,14.13,2,12,2C6.48,2,2,6.48,2,12 c0,5.52,4.48,10,10,10s10-4.48,10-10c0-1.19-0.22-2.33-0.6-3.39L19.79,10.22z"/></svg>

              </div>

              <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" absolute right-0 appearance-none">

            </div>

   <!-- option-3 -->
              <div @click="option3Selected=!option3Selected" id="popup-8-option-1" :class="`${option3Selected && ' bg-[#928bc0b3] !text-white border-[#EBBC42]' } bg-white text-[#261641]/80   w-full rounded-[12px] transition-colors ease-out  md:min-h-[80px] cursor-pointer border border-transparent flex items-center  space-x-3  py-2 md:py-0 relative min-h-[50px] shadow-[0_0_3px_white]   font-semibold px-2 md:px-4`">

              <!-- option circle -->

              <!-- <span class="rounded-full flex justify-center items-center text-center w-[27px] min-h-[27px] md:w-[32px] md:h-[32px] bg-[#F6F6F6] text-lg  font-medium text-[#005C7D] ">

                <span id="popup-8-choice-1"
                ref="option3"  :class="`${!option3Selected && 'opacity-0 '} transition-opacity ease-in-out w-[17px] h-[17px]  md:w-[60%] md:h-[60%]  rounded-full bg-white shadow-[1px_2px_3px_rgba(0,0,0,0.14)]`"></span>

                </span> -->

              <!-- option content  -->

                 <div class="flex justify-between w-full">
              <span class="text-sm md:text-base font-semibold ">Lorem ipsum dolor sit amet C </span>

              <!-- icon  -->
             <svg :class="`hidden text-[#EBBC42] transition-opacity ease-in-out opacity-0 ${option3Selected && 'opacity-100'} `" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M22,5.18L10.59,16.6l-4.24-4.24l1.41-1.41l2.83,2.83l10-10L22,5.18z M19.79,10.22C19.92,10.79,20,11.39,20,12 c0,4.42-3.58,8-8,8s-8-3.58-8-8c0-4.42,3.58-8,8-8c1.58,0,3.04,0.46,4.28,1.25l1.44-1.44C16.1,2.67,14.13,2,12,2C6.48,2,2,6.48,2,12 c0,5.52,4.48,10,10,10s10-4.48,10-10c0-1.19-0.22-2.33-0.6-3.39L19.79,10.22z"/></svg>

              </div>

              <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" absolute right-0 appearance-none">

            </div>

   <!-- option-4 -->

              <div @click="e=>{

              option4Selected=!option4Selected
              } " id="popup-8-option-1" :class="`${option4Selected && 'bg-[#928bc0b3] !text-white border-[#EBBC42]' } bg-white text-[#261641]/80  w-full rounded-[12px] transition-colors ease-out  md:min-h-[80px] cursor-pointer border border-transparent flex items-center  space-x-3  py-2 md:py-0 relative min-h-[50px] shadow-[0_0_3px_white]   px-2 md:px-4 font-semibold group`">

              <!-- option  -->

              <!-- <span class="rounded-full flex justify-center items-center text-center w-[27px] min-h-[27px] md:w-[32px] md:h-[32px] bg-[#F6F6F6]  text-lg  font-medium text-[#005C7D] ">
                <span id="popup-8-choice-1"
                ref="option4"  :class="`${!option4Selected && 'opacity-0 '} transition-opacity ease-in-out bg-white w-[17px] h-[17px]  md:w-[60%] md:h-[60%]   rounded-full shadow-[1px_2px_3px_rgba(0,0,0,0.14)]`"></span>


                </span> -->

              <!-- option content  -->

             <div class="flex justify-between w-full">
              <span class="text-sm md:text-base font-semibold ">Lorem ipsum dolor sit amet C </span>

              <!-- icon  -->
           <svg :class="`hidden text-[#EBBC42] transition-opacity ease-in-out opacity-0 ${option2Selected && 'opacity-100'} `" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M22,5.18L10.59,16.6l-4.24-4.24l1.41-1.41l2.83,2.83l10-10L22,5.18z M19.79,10.22C19.92,10.79,20,11.39,20,12 c0,4.42-3.58,8-8,8s-8-3.58-8-8c0-4.42,3.58-8,8-8c1.58,0,3.04,0.46,4.28,1.25l1.44-1.44C16.1,2.67,14.13,2,12,2C6.48,2,2,6.48,2,12 c0,5.52,4.48,10,10,10s10-4.48,10-10c0-1.19-0.22-2.33-0.6-3.39L19.79,10.22z"/></svg>

              </div>

              <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" absolute right-0 appearance-none">

            </div>

          </section>

<!-- when Address information required  -->

  <section v-if="currentScreen==3" class="space-y-3">

  <input type="text" placeholder="Street Address"
            class="placeholder-black/80 text-[#261641] px-2 focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]   text-sm md:text-base bg-white shadow-[0_0_3px_white] border border-transparent focus:border-[#EBBC42] md:px-4">

  <input type="text" placeholder="Street Address Line 2"
            class="placeholder-black/80 text-[#261641] px-2 focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]   text-sm md:text-base bg-white shadow-[0_0_3px_white] border border-transparent focus:border-[#EBBC42] md:px-4">

  <input type="text" placeholder="City"
            class="placeholder-black/80 text-[#261641] px-2 focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]   text-sm md:text-base bg-white shadow-[0_0_3px_white] border border-transparent focus:border-[#EBBC42] md:px-4">

  <input type="text" placeholder="State / Province"
            class="placeholder-black/80 text-[#261641] px-2 focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]   text-sm md:text-base bg-white shadow-[0_0_3px_white] border border-transparent focus:border-[#EBBC42] md:px-4 ">

  <input type="text" placeholder="Postal / Zip Code"
            class="placeholder-black/80 text-[#261641]  focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]   text-sm md:text-base bg-white shadow-[0_0_3px_white] border border-transparent focus:border-[#EBBC42] px-2 md:px-4">


    </section>

<!-- when email information required  -->

 <section v-if="currentScreen==4" class="space-y-3">

         <input type="email" placeholder="Email@mail.com.."
            class="placeholder-black/80 text-[#261641] px-2 focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]   text-sm md:text-base bg-white shadow-[0_0_3px_white] border border-transparent focus:border-[#EBBC42] md:px-4 ">

  </section>

   <!-- when phone number information required  -->
   <section v-if="currentScreen==5" class="space-y-3">
         <input type="number" placeholder="(XXX)(XXXXXXX)
"
            class="placeholder-black/80 text-[#261641] px-2 focus:ring-0 focus:outline-none rounded-[12px] w-full  min-h-[50px] md:min-h-[80px]   text-sm md:text-base bg-white shadow-[0_0_3px_white] border border-transparent focus:border-[#EBBC42] md:px-4">

   </section>


     <!-- when dropdown information required  -->

        <section v-if="currentScreen==6" class=" relative">
            <select
              class="block appearance-none w-full  border border-transparent min-h-[50px] md:min-h-[80px]  px-4 pr-8 rounded-[12px] leading-tight focus:outline-none  text-[#261641] text-sm md:text-base bg-white focus:border-[#EBBC42]"
              id="grid-state ">

              <option  value="" disabled selected hidden>Please Select</option>
              <option>Option 1</option>
              <option>Option 2</option>
            </select>
            <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-[#261641]">
              <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
                <path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z" />
              </svg>
            </div>
          </section>

      <!-- When yes or No information needed (Power Type)  -->

         <section v-if="currentScreen==7" class="mx-auto w-fit">
            <button class=" w-fit px-6 py-2 md:px-0 md:py-0 border-transparent bg-white md:w-[160px] border  md:h-[60px] rounded-lg transition-colors ease-in-out  text-[#261641] xl:hover:bg-[rgb(220,215,255,0.7)] xl:hover:text-white text-base md:text-xl mx-2 lg:hover:border-[#EBBC42] ">Yes</button>

            <button class=" w-fit px-6 py-2 md:px-0 md:py-0 border-transparent bg-white md:w-[160px] border  md:h-[60px] rounded-lg transition-colors ease-in-out  text-[#261641] xl:hover:bg-[rgb(220,215,255,0.7)] xl:hover:text-white  lg:hover:border-[#EBBC42] text-base md:text-xl mx-2">No</button>
          </section>

     <!-- When short information needed (General Type short box)  -->

   <section v-if="currentScreen==8" class="space-y-3">

      <textarea autofocus name="" id="" cols="30" rows="3" placeholder="Type a short description here....." class="placeholder-black/80 p-3 focus:ring-0 focus:outline-none rounded-[12px] w-full border border-transparent [resize:none] min-h-[50px] focus:border-[#EBBC42] shadow-[0_0_3px_white] bg-white text-[#261641] text-sm md:text-base"></textarea>

   </section>

   <!-- When detailed information needed (General Type long box)  -->

   <section v-if="currentScreen==9" class="space-y-3">


     <textarea autofocus name="" id="" cols="30" rows="15" placeholder="Type a long description here....." class="placeholder-black/80 p-3 focus:ring-0 focus:outline-none rounded-[12px] w-full  border border-transparent [resize:none] min-h-[50px] focus:border-[#EBBC42] shadow-[0_0_3px_white] bg-white text-[#261641] text-sm md:text-base"></textarea>

   </section>

   </main>

<!-- Next Button  -->

      <button @click="nextQuestion" class="mx-auto block px-8 py-3  md:text-2xl transition-colors ease-in-out text-white xl:text-white/80 bg-black/70 border xl:hover:bg-white xl:hover:text-black active:bg-[#1E3253] rounded-[12px] w-full border-[#62789c]">Next</button>

 </section>

<footer class="text-white flex  items-center w-full flex-col py-5   xl:py-8 px-2 space-y-2 text-xs md:text-sm">

  <p class=" popins ">Copyright © My Company. All Rights Reserved. </p>

  <p class=""><a href="">Terms of Service</a> | <a href="">Privacy Policy</a> | <a href="">Contact Us</a></p>


</footer>

</div>
</template>

<script>
export default {
name:'QuizformaBaseTemplate',
data(){
  return{
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


    if(this.currentScreen < this.totelQuizScreens){
this.currentScreen++
    }
//  this.$refs.next.classList.add('active:text-white active:bg-[rgb(220,215,255,0.7)]')

  },
  previousQuestion(){

    if(this.currentScreen!=1)  this.currentScreen--

  },


}
}
</script>

<style>

</style>