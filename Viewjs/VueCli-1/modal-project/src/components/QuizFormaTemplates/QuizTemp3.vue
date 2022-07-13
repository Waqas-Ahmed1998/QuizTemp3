<template>
<div class="min-h-screen bg-[#E5E5E5] md:pt-16">


<!-- logo  -->
<!-- <header class="py-3 md:py-4">
    <img src="../../assets/QuizformLogoBlack.svg" alt="" class="scale-[0.7] w-32 mx-auto  md:w-auto ">
</header> -->

  <div id="popup-1" class="">

    <div class=" w-full md:max-w-[735px]   ease-in-out   md:min-h-[569px] flex flex-col    bg-white
  md:shadow-[0_4px_10px_rgba(0,0,0,0.12)] min-h-fit  md:mx-auto  montserat relative  md:rounded-md pt-4 pb-6 md:py-5 ">

<!-- top content  -->
      <div class="flex flex-col relative space-y-3   ">
        <p class=" px-4 tracking-wide text-base md:xl popins text-[#FF6247] font-semibold" > <span>{{currentScreen}} out of {{totelQuizScreens}}</span>
           </p>

<!-- progress bar  -->
  <div class="block   h-1 bg-black/10 rounded-r-md w-full ">
        <div :class="` w-[15%] h-1 bg-[#FF6247] rounded-r-md`"></div>
   </div>
      </div>

      <!-- middle content  -->

      <main class=" relative  px-5    md:w-[100%] mx-auto  ">


        <div class="flex flex-col items-center pt-4 pb-8 self-start  ">



          <h2 class="text-center text-2xl md:text-[36px] popins text-[#1A6F6F] font-bold md:leading-[46px] mb-3 md:mb-4">When are you hoping
            to
            have
            the project
            completed by?</h2>

          <p class=" text-center text-base md:xl popins text-[#1A6F6F]/70  font-semibold" >When are you hoping
            to
            have
            the project
            completed by?</p>

<!-- section contains all different inputs   -->

          <section class=" mt-6 text-sm w-full md:w-[584px]   ">

  <!-- options information  -->
            <section v-if="currentScreen==1">
             <div
             @click="option1Selected=!option1Selected"  :class="` cursor-pointer  flex flex-col  w-full    relative my-3 `">

            <!-- option content  -->
              <div :class="`flex items-center justify-between  placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light  w-full min-h-[50px] border-2 border-transparent text-center px-3 py-4  rounded-[6px] bg-[#F5F5F5] ${option1Selected && '  border-[#FF6247]'}  `">
                <span class="text-sm md:text-base font-semibold ">Lorem ipsum dolor sit amet A </span>

              <!-- icon  -->
                 <svg :class="`hidden text-[#EBBC42] transition-opacity ease-in-out opacity-0 ${option1Selected && 'opacity-100'} `" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M22,5.18L10.59,16.6l-4.24-4.24l1.41-1.41l2.83,2.83l10-10L22,5.18z M19.79,10.22C19.92,10.79,20,11.39,20,12 c0,4.42-3.58,8-8,8s-8-3.58-8-8c0-4.42,3.58-8,8-8c1.58,0,3.04,0.46,4.28,1.25l1.44-1.44C16.1,2.67,14.13,2,12,2C6.48,2,2,6.48,2,12 c0,5.52,4.48,10,10,10s10-4.48,10-10c0-1.19-0.22-2.33-0.6-3.39L19.79,10.22z"/></svg>
              </div>

<!-- bottom shadow  -->
               <div
                :class="`${option1Selected && '  hidden'}  absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] `">
              </div>
                 <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" absolute right-0 appearance-none">
            </div>

            <div
             @click="option2Selected=!option2Selected"  :class="` cursor-pointer  flex flex-col  w-full    relative my-3 `">

            <!-- option content  -->
              <div :class="`flex items-center justify-between  placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light  w-full min-h-[50px] border-2 border-transparent text-center px-3 py-4  rounded-[6px] bg-[#F5F5F5] ${option2Selected && '  border-[#FF6247]'}  `">
                <span class="text-sm md:text-base font-semibold ">Lorem ipsum dolor sit amet B </span>

              <!-- icon  -->
                 <svg :class="` hidden text-[#EBBC42] transition-opacity ease-in-out opacity-0 ${option2Selected && 'opacity-100'} `" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M22,5.18L10.59,16.6l-4.24-4.24l1.41-1.41l2.83,2.83l10-10L22,5.18z M19.79,10.22C19.92,10.79,20,11.39,20,12 c0,4.42-3.58,8-8,8s-8-3.58-8-8c0-4.42,3.58-8,8-8c1.58,0,3.04,0.46,4.28,1.25l1.44-1.44C16.1,2.67,14.13,2,12,2C6.48,2,2,6.48,2,12 c0,5.52,4.48,10,10,10s10-4.48,10-10c0-1.19-0.22-2.33-0.6-3.39L19.79,10.22z"/></svg>
              </div>

<!-- bottom shadow  -->
              <div
                :class="`${option2Selected && '  hidden'}  absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] `">
              </div>
                 <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" absolute right-0 appearance-none">
            </div>

            <div
             @click="option3Selected=!option3Selected"  :class="` cursor-pointer  flex flex-col  w-full    relative my-3 `">

            <!-- option content  -->
              <div :class="`flex items-center justify-between  placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light  w-full min-h-[50px] border-2 border-transparent text-center px-3 py-4  rounded-[6px] bg-[#F5F5F5] ${option3Selected && '  !border-[#FF6247]'}  `">
                <span class="text-sm md:text-base font-semibold ">Lorem ipsum dolor sit amet C </span>

              <!-- icon  -->
                 <svg :class="` hidden text-[#EBBC42] transition-opacity ease-in-out opacity-0 ${option3Selected && 'opacity-100'} `" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M22,5.18L10.59,16.6l-4.24-4.24l1.41-1.41l2.83,2.83l10-10L22,5.18z M19.79,10.22C19.92,10.79,20,11.39,20,12 c0,4.42-3.58,8-8,8s-8-3.58-8-8c0-4.42,3.58-8,8-8c1.58,0,3.04,0.46,4.28,1.25l1.44-1.44C16.1,2.67,14.13,2,12,2C6.48,2,2,6.48,2,12 c0,5.52,4.48,10,10,10s10-4.48,10-10c0-1.19-0.22-2.33-0.6-3.39L19.79,10.22z"/></svg>
              </div>

<!-- bottom shadow  -->
              <div
                :class="` ${option3Selected && ' hidden'}  absolute  -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] `">
              </div>
                 <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" absolute right-0 appearance-none">
            </div>

                     <div
             @click="option4Selected=!option4Selected"  :class="` cursor-pointer  flex flex-col  w-full    relative my-3 `">

            <!-- option content  -->
              <div :class="`flex items-center justify-between  placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light  w-full min-h-[50px] border-2 border-transparent text-center px-3 py-4  rounded-[6px] bg-[#F5F5F5] ${option4Selected && '  border-[#FF6247]'}  `">
                <span class="text-sm md:text-base font-semibold ">Lorem ipsum dolor sit amet D </span>

              <!-- icon  -->
                 <svg :class="` hidden text-[#EBBC42] transition-opacity ease-in-out opacity-0 ${option4Selected && 'opacity-100'} `" xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M22,5.18L10.59,16.6l-4.24-4.24l1.41-1.41l2.83,2.83l10-10L22,5.18z M19.79,10.22C19.92,10.79,20,11.39,20,12 c0,4.42-3.58,8-8,8s-8-3.58-8-8c0-4.42,3.58-8,8-8c1.58,0,3.04,0.46,4.28,1.25l1.44-1.44C16.1,2.67,14.13,2,12,2C6.48,2,2,6.48,2,12 c0,5.52,4.48,10,10,10s10-4.48,10-10c0-1.19-0.22-2.33-0.6-3.39L19.79,10.22z"/></svg>
              </div>

<!-- bottom shadow  -->
              <div
                :class="`${option4Selected && '  hidden'}  absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] `">
              </div>
                 <!-- input  -->
              <input id="option-1-input" name="option-1" value="choice-1" type="checkbox"
                class=" absolute right-0 appearance-none">
            </div>

            </section>

            <!-- personal information  -->

            <section v-if="currentScreen==2">
            <div
              class=" flex flex-col  w-full bg-[#F5F5F5] border-none outline-none  rounded-[6px] px-4 relative py-1 my-3">
              <input type="text" placeholder="First Name "
                class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none  ">


              <div
                class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
              </div>
            </div>

            <div
              class=" flex flex-col  w-full bg-[#F5F5F5] border-none outline-none  rounded-[6px] px-4 relative py-1 my-3 ">
              <input type="text" placeholder="Last Name "
                class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none  ">

              <div
                class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
              </div>
            </div>

            </section>

            <!-- address information  -->

     <section v-if="currentScreen==3">
              <div
                class="flex flex-col  w-full  border-none outline-none   relative  my-3 ">
                <input type="text" placeholder="Street Number"
                  class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 ">

                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>

          <div
                class="flex flex-col  w-full  border-none outline-none   relative  my-3 ">
                <input type="text" placeholder="Street Number Line 2"
                  class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 ">

                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>

          <div
                class="flex flex-col  w-full  border-none outline-none   relative  my-3 ">
                <input type="text" placeholder="City"
                  class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 ">

                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>

            <div
                class="flex flex-col  w-full  border-none outline-none   relative  my-3 ">
                <input type="text" placeholder="State / Province"
                  class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 ">

                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>

            <div
                class="flex flex-col  w-full  border-none outline-none     my-3 relative ">

                <input type="text" placeholder="Postal / ZipCode"
                  class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 ">

                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>



            </section>

<!-- Drop down information  -->
           <section v-if="currentScreen==4" class="flex flex-col justify-center  ">


              <div class=" relative flex flex-col  w-full  border-none outline-none     my-3 ">
                <select
                  class="block appearance-none w-full placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none    border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3  "
                  id="grid-state ">
                  <option value="" disabled selected hidden>Please Select</option>
                  <option>Option 1</option>
                  <option>Option 2</option>
                </select>
                <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
                  <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
                    <path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z" />
                  </svg>
                </div>

                 <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>

            </section>

       <!-- email information  -->

       <section v-if="currentScreen==5" >
          <div
                class="flex flex-col  w-full  border-none outline-none   relative  my-3 ">
                <input type="text" placeholder="example@mail.com"
                  class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 ">

                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>
       </section>
   <!-- phone Number information  -->
          <section v-if="currentScreen==6" >
          <div
                class="flex flex-col  w-full  border-none outline-none   relative  my-3 ">
                <input type="number" placeholder="(XXX) XXX-XXXX"
                  class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 ">

                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>
       </section>
   <!-- short answer information  -->
          <section v-if="currentScreen==7" >
          <div
                class="flex flex-col  w-full  border-none outline-none   relative  my-3 ">
                   <textarea autofocus name="" id="" cols="30" rows="3" placeholder="Type a short description here....."   class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 [resize:none]"></textarea>


                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>
       </section>
   <!-- detail answer information  -->

             <section v-if="currentScreen==8" >
          <div
                class="flex flex-col  w-full  border-none outline-none   relative  my-3 ">
                   <textarea autofocus name="" id="" cols="30" rows="13" placeholder="Type a short description here....."   class="placeholder-[#A5A5A5] italic text-sm md:text-xl popins font-light   focus:ring-0 focus:outline-none  w-full  border  min-h-[50px] bg-transparent border-none outline-none bg-[#F5F5F5] rounded-[6px] py-[14px] px-3 [resize:none]"></textarea>


                <div
                  class="absolute -bottom-0 border border-[#9A9A9A] w-[98%] rounded-full left-[50%] translate-x-[-50%] ">
                </div>
              </div>
       </section>

<!-- Yes or no infromation  -->
       <section v-if="currentScreen==9" class="mx-auto w-fit mt-4">
            <button class=" w-fit px-6 py-2 md:px-0 md:py-0 border-transparent bg-[#88C7E8] md:w-[160px] border  md:h-[60px] rounded-lg transition-colors ease-in-out  text-white xl:hover:bg-white xl:hover:text-black text-base md:text-xl mx-2 lg:hover:border-[#FF6247] ">Yes</button>

            <button class=" w-fit px-6 py-2 md:px-0 md:py-0 border-transparent bg-[#88C7E8] md:w-[160px] border  md:h-[60px] rounded-lg transition-colors ease-in-out  text-white xl:hover:bg-white xl:hover:text-black  lg:hover:border-[#FF6247] text-base md:text-xl mx-2">No</button>
       </section>

             <!-- options information  -->



            <!-- next button  -->
              <Button
              @click="goToNext" class="active:bg-[#1A6F6F] bg-[#FF6247] mt-16 px-8 py-3 text-base  md:text-xl text-white rounded-md popins font-semibold block mx-auto">Next</Button>
          </section>
        </div>

      </main>

<!-- previous arrow  -->

  <div @click="goToPrevious" class=" scale-[0.8] md:scale-[1] absolute left-0 bottom-2 md:bottom-3 space-x-3  flex items-center group cursor-pointer px-4 w-fit ">

        <svg class=" xl:group-hover:text-[#FF6247]  text-black cursor-pointer transition-colors ease-out xl:hover:text-[#261641]"  xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="currentColor"><rect fill="none" height="24" width="24"/><path d="M9,19l1.41-1.41L5.83,13H22V11H5.83l4.59-4.59L9,5l-7,7L9,19z"/></svg>
          <button id="" class="hidden md:inline-block text-xs md:text-sm text-[#818181]">Previous</button>
        </div>
    </div>


    <footer class="  text-black flex mt-4  items-center w-full flex-col py-5   xl:py-8 px-2 space-y-2 text-xs ">
      <img src="../../assets/QuizformLogoBlack.svg" alt="" class="scale-[0.7] w-32   md:w-auto ">

      <p class=" popins ">Copyright © My Company. All Rights Reserved. </p>

      <p class=""><a href="">Terms of Service</a> | <a href="">Privacy Policy</a> | <a href="">Contact Us</a></p>


    </footer>
  </div>
</div>

</template>

<script>
export default {
name:'QuizTemp3',
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
  goToNext(){
    if(this.currentScreen < this.totelQuizScreens)  this.currentScreen++
  },
  goToPrevious(){

    if(this.currentScreen!=1)  this.currentScreen--

  },


}
}
</script>

<style>

</style>