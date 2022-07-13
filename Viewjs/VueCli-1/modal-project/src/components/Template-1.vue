<template>
  <body class="">

  <div class="tw-bg-black/90 tw-relative tw-min-h-screen tw-mx-auto  tw-items-center  tw-overflow-hidden ">
<!-- <button v-show="!bulletVideoVer" @click="showVideo=!showVideo" class="tw-absolute tw-top-2 tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md">Toggle Video</button>

<button v-show="!bulletVideoVer" @click="showBullets=!showBullets" class="tw-absolute tw-top-14 tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md">Toggle Bullet</button>

<button @click="showButton=!showButton" class="tw-absolute tw-top-28 tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md">Toggle Button</button>

<button @click="videoDescription=!videoDescription" class="tw-absolute tw-top-40 tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md">Toggle Video Desc</button> -->

<!-- main layouts  -->

<!-- <button   @click="basicHandler()" :class="!split && !max && !full && 'tw-bg-[#704EDF] tw-text-white'" class=" tw-absolute tw-top-40  tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md">Basic Layout</button>

<button  @click="splitHandler()" :class="split && 'tw-bg-[#704EDF] tw-text-white'" class="tw-absolute tw-top-2  tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md">Split Layout</button>

<button  @click="fullHandler()" :class="full && 'tw-bg-[#704EDF] tw-text-white'" class="tw-absolute tw-top-14  tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md">Full Layout</button>

<button  @click="maxHandler()" :class="max && 'tw-bg-[#704EDF] tw-text-white'" class="tw-absolute tw-top-28  tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md  ">Max Layout</button> -->

<!-- layout side bar  -->

<div class="tw-hidden lg:tw-block tw-absolute tw-top-[10px] tw-space-y-3 tw-right-2 tw-flex tw-flex-col tw-text-center ">

<div class="tw-flex tw-flex-col tw-text-center tw-space-y-2">
<span class="tw-text-white">Main Templates</span>

<button   @click="basicHandler()" :class="!split && !max && !full && 'tw-bg-[#704EDF] tw-text-white'" class="  tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md md:tw-w-[170px]">lead Layout</button>

<button  @click="splitHandler()" :class="split && 'tw-bg-[#704EDF] tw-text-white'" class="tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md  md:tw-w-[170px]">Split Layout</button>

<button  @click="fullHandler()" :class="full && 'tw-bg-[#704EDF] tw-text-white'" class="tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md md:tw-w-[170px]">Full Layout</button>

<button  @click="maxHandler()" :class="max && 'tw-bg-[#704EDF] tw-text-white'" class=" tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md md:tw-w-[170px] ">Max Layout</button>
</div>

<!-- desktop sizes  -->
<div class="tw-flex tw-flex-col tw-text-center tw-space-y-2 ">
<span class="tw-text-white">Template Sizes</span>
<button    @click="templateMaxHandler()" :class="templateMax && 'tw-bg-[#704EDF]  tw-text-white'" class=" active:tw-bg-blue-200  tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md md:tw-w-[170px] ">Default</button>

<button    @click="templateMdHandler()" :class="templateMd &&  'tw-bg-[#704EDF]  tw-text-white'"   class=" active:tw-bg-blue-200  tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md md:tw-w-[170px] ">Large</button>
<button v-if="!split"   @click="templateSmHandler()" :class=" templateSm && 'tw-bg-[#704EDF]  tw-text-white'"   class=" active:tw-bg-blue-200   tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md md:tw-w-[170px]  ">Medium</button>
<button  v-if="!max && !split"  @click="templateXsHandler()" :class=" templateXs && 'tw-bg-[#704EDF]  tw-text-white'"   class=" active:tw-bg-blue-200   tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md md:tw-w-[170px]  ">Small</button>


</div>
<!-- Template Variations  -->

<div v-if="split || full || max" class="tw-flex tw-flex-col tw-text-center tw-space-y-2">
<span class="tw-text-white">Template Variations</span>


<button ref="showImage" v-text="showImageText"   @click="showImageHandler()"  class=" tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md active:tw-bg-blue-200 md:tw-w-[170px]"></button>

<button  v-text="btnTopButtonText" @click="topButtonHandler()"  class=" tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md active:tw-bg-blue-200 md:tw-w-[170px]"></button>

<button v-text="splitBtnText" ref="btnSwapBullet"  @click="splitBulletSwapHandler()"  class=" active:tw-bg-blue-200   tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md  md:tw-w-[170px]"></button>
</div>
</div>


<!-- <button v-show="showVideo && showBullets" @click="BulletVideoHandler()" class="tw-absolute  tw-top-80 tw-right-2 tw-px-4 tw-py-2 tw-bg-purple-200 tw-rounded-md">Video & Bullets Variation</button> -->

<!-- : templateXs || templateSm || templateMd ? 'tw-shadow-md tw-shadow-white' -->

<!-- tw-shadow-white tw-shadow-sm tw-border-white -->

    <Popup1 :show='show' @close='closePopup()'/>

    <div
    ref="templateWidth"
    :class=" showBullets ||showVideo ||split ||max ||full ? 'md:!tw-mt-2  '  : 'md:tw-mt-14 '"
      class=" tw-mx-auto  tw-rounded-sm tw-max-w-[1170px] md:tw-py-3     tw-relative   tw-items-center tw-justify-center  tw-bg-black">

<!-- Lead content  -->

      <div
        class=" md:tw-p-0 lg:tw-px-10 tw-bg-transparent tw-w-full tw-px-1 tw-flex tw-flex-col tw-items-center tw-pt-5 md:tw-py-0 tw-relative tw-z-[3] md:tw-top-auto tw-mx-auto  tw-text-center  ">

        <p
          class="  tw-text-center md:tw-py-2  tw-px-1 tw-font-normal tw-text-lg tw-leading-[22px] md:tw-text-2xl lg:tw-text-[28px] tw-text-[#fbfbfb]  subheading w-fit  ">
          This Is The Subheadline Above The Main Headline</p>
<!-- tw-text-2xl  -->
        <h2

          class=" tw-text-[28px] tw-leading-[28px] md:tw-text-4xl lg:tw-text-[58px] md:tw-leading-[1.1]   tw-py-2  md:tw-py-4  tw-text-center  heading tw-font-bold tw-text-transparent tw-bg-clip-text  tw-bg-gradient-to-r  tw-from-[#fb01b4] tw-via-[#d278d3] tw-to-[#1dffe1] tw-tracking-[-1px] ">

          Create Amazing Pages Just Like This! It Starts With The Headline!

        </h2>

        <p class="  tw-text-lg tw-leading-[22px] lg:tw-text-2xl  tw-py-2 md:tw-py-4  call  tw-text-[#ffffff]  ">
          Call To Action Statement Goes Here!</p>


        <form @submit.prevent action=""
          class="tw-flex tw-flex-col md:tw-px-5 tw-justify-center tw-w-full tw-px-1 md:tw-w-[95%] tw-space-y-6  tw-rounded-md  tw-mb-2 tw-mt-0  tw-items-center ">



          <input type="email" placeholder="Your Email Address Here ..."
            class="tw-hidden tw-outline-none tw-border focus:tw-border-[#921dbd] tw-rounded-md tw-w-full lg:tw-w-[80%]  tw-shadow-sm tw-text-black text-sm md:text-base  tw-px-4 tw-py-3 ">



          <div v-if="!showButton" class="tw-group">

            <button
:class="templateXs && 'sm:group-hover:!tw-px-6 '"
            @click="clickHandler()"
              class="tw-cursor-pointer tw-bg-[#6438F8] hover:tw-bg-[#704edf]  tw-text-white tw-border-8 tw-border-transparent  tw-font-bold   hover:tw-animate-none  tw-py-2 md:tw-py-4 md:tw-px-4 md:tw-text-4xl tw-w-full md:tw-w-fit tw-flex btn tw-space-x-2 md:tw-space-x-4  tw-justify-center tw-items-center tw-transition-all sm:group-hover:tw--translate-y-3 sm:hover:tw-px-10  tw-ease-in-out tw-text-xl tw-rounded-full  ">


              <p class="">GET INSTANT ACCESS NOW!</p>

            </button>

          </div>

          <p
          v-show="!showVideo && !showBullets && !max && !split && !full"
            class=" tw-align-baseline tw-text-xs md:tw-text-sm tw-text-center tw-font-medium disclaimer tw-text-[#fdfdfd] ">
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

      <!-- when switching to advance options  -->

      <div  class="tw-mt-5 md:tw-mt-10" >

        <!-- Default  -->

        <!-- <div v-if="full && !this.split && !this.max" ref="variation" :class="showVideo && showBullets && 'md:tw-space-x-10'" class="tw-flex tw-flex-col md:tw-flex-row ">

          <div v-if="showVideo"  class="tw-w-full">
              <VideoVue :withVideo="showVideo" :bulletVideoVer="bulletVideoVer" :videoDescription="videoDescription" :onlyVideo="!showBullets"/>
          </div>
          <div v-if="showBullets" class="tw-w-full">
              <BulletsVue/>
          </div>

        </div> -->

        <!-- split  -->

          <div v-if="split && !max && !full" :class="splitBulletSwap && 'md:tw-flex-row-reverse'" class="tw-flex tw-flex-col md:tw-flex-row md:tw-space-x-10">

          <div :class="split && templateMd && 'md:tw-pl-8 '"  class="tw-w-full md:tw-mt-2">
              <VideoVue v-if='splitVideo'/>
              <ImageVue v-if='!splitVideo'/>
          </div>
          <div  class="tw-w-full">
              <BulletsVue/>
          </div>

        </div>

        <!-- Full  -->

          <div v-if="full && !split && !max" class="tw-flex tw-flex-col">

          <div  class="tw-w-full">
              <VideoVue :full='full' :templateXs='templateXs'/>
          </div>
          <div  class="tw-w-full">
              <BulletsVue/>
          </div>

        </div>

          <!-- Max  -->

          <div v-if="max" class="tw-flex tw-flex-col ">
              <div :class="templateSm && max && 'md:!tw-flex-col tw-justify-center '" class="tw-flex md:tw-flex-row tw-flex-col tw-space-y-4 md:tw-space-y-0">
                <div class="tw-w-full ">
                  <ImageVue :templateSm='templateSm' :max='max' :templateMd='templateMd'/>
                  </div>
                  <div  class="tw-w-full">
                    <BulletsVue/>
                </div>
              </div>
                <div class="md:tw-mt-10">
                  <VideoVue :max='max'/>
                </div>
        </div>

<!-- bottom button code with disclaimer  -->

        <div  v-if="showBullets || showVideo ||split ||max||full">
           <button
            @click="clickHandler()"
              class="tw-mt-4 md:tw-mt-10 tw-mx-auto tw-cursor-pointer tw-bg-[#6438F8] hover:tw-bg-[#704edf]  tw-text-white tw-border-8 tw-border-transparent  tw-font-bold   hover:tw-animate-none  tw-py-2 md:tw-py-4 md:tw-px-4 md:tw-text-4xl tw-w-full md:tw-w-fit tw-flex btn tw-space-x-2 md:tw-space-x-4  tw-justify-center tw-items-center tw-transition-all sm:group-hover:tw--translate-y-3 sm:group-hover:tw-px-10  tw-ease-in-out tw-text-xl tw-rounded-full ">

              <p class="">GET INSTANT ACCESS NOW!</p>

            </button>
              <p
            class=" tw-text-white tw-text-xs tw-text-center tw-mt-4">
            We respect
            your
            privacy,
            Your
            email

            never be
            shared or sold</p>
            </div>
      </div>

    </div>

  </div>

</body>
</template>

<script>
import BulletsVue from './Bullets.vue';
import Popup1 from './Popup1.vue';
import VideoVue from './Video.vue';
import ImageVue from './Image.vue';
export default {
    name: "Template-1",
      components: {
    Popup1,
    VideoVue,
    BulletsVue,
ImageVue
},
data() {
  return {
    show: false,
    showVideo:false,
    showBullets:false,
    showButton:false,
    videoDescription:false,
    bulletVideoVer:false,
    full:false,
    split:false,
    max:false,
    splitBulletSwap:false,
    splitBtnText:'Bullets To Left',
    splitVideo:true,
    showImageText:'Show Image',
    btnTopButtonText:'Remove Top Button',

    templateXs:false,
    templateSm:false,
    templateMd:false,
    templateMax:true,

  }
},
    methods: {
splitHandler(){
      this.templateSizeReset()
  this.split=true;
  this.full=false;
  this.max=false;
},
fullHandler(){
      this.templateSizeReset()
  this.split=false;
  this.full=true;
  this.max=false;
},
maxHandler(){
      this.templateSizeReset()
  this.split=false;
  this.full=false;
  this.max=true;
},

basicHandler()
 {

  this.templateSizeReset()

    this.split=false;
  this.full=false;
  this.max=false;
 },

// inside main layout tempalte variations

 splitBulletSwapHandler(){
this.splitBulletSwap=!this.splitBulletSwap
if(this.splitBtnText=='Bullets To Left')
{
  this.splitBtnText='Bullets To Right'
}else {

  this.splitBtnText='Bullets To Left'
}

 },

 showImageHandler(){
  this.splitVideo=!this.splitVideo
if(this.showImageText=='Show Image'){

  this.showImageText='Show Video'
}else {
  this.showImageText='Show Image'

}
 },

 topButtonHandler(){
this.showButton=!this.showButton
if(this.btnTopButtonText== 'Remove Top Button'){
  this.btnTopButtonText='Add Top Button'
}else {
  this.btnTopButtonText='Remove Top Button'
}
 },

// Tempalates sizes handlers

templateXsHandler(){

  this.templateXs=true
  this.templateMax=false
  this.templateMd=false
this.templateSm=false

  this.$refs.templateWidth.classList.add('tw-shadow-[0_0_2px_white]')

// this.$refs.templateWidth.classList.add('tw-shadow-[0.5px_0.5px_3px_white]')
/
  this.$refs.templateWidth.classList.remove('tw-max-w-[1170px]')
  this.$refs.templateWidth.classList.remove('tw-max-w-[1120px]')
  this.$refs.templateWidth.classList.remove('tw-max-w-[900px]')
this.$refs.templateWidth.classList.add('tw-max-w-[650px]')

},

templateSmHandler(){


   this.templateXs=false
  this.templateMax=false
  this.templateMd=false
this.templateSm=true

// this is to add shadow/border when template side reduced from default
  this.$refs.templateWidth.classList.add('tw-shadow-[0_0_2px_white]')

// this.$refs.templateWidth.classList.add('tw-shadow-[0.5px_0.5px_3px_white]')

// to new max width to template and removed any previous max width added in order to work template size buttons

  this.$refs.templateWidth.classList.remove('tw-max-w-[1170px]')
  this.$refs.templateWidth.classList.remove('tw-max-w-[1120px]')
  this.$refs.templateWidth.classList.remove('tw-max-w-[650px]')
this.$refs.templateWidth.classList.add('tw-max-w-[900px]')

},
templateMdHandler(){


   this.templateXs=false
   this.templateMax=false
    this.templateSm=false
    this.templateMd=true

// this is add shadow when template side reduced from default
  this.$refs.templateWidth.classList.add('tw-shadow-[0_0_2px_white]')
  // this.$refs.templateWidth.classList.add('tw-shadow-[0.5px_0.5px_3px_white]')

// to new max width to template and removed any previous max width added in order to work template size buttons

   this.$refs.templateWidth.classList.remove('tw-max-w-[1170px]')
  this.$refs.templateWidth.classList.remove('tw-max-w-[900px]')
  this.$refs.templateWidth.classList.remove('tw-max-w-[650px]')
this.$refs.templateWidth.classList.add('tw-max-w-[1120px]')

},
templateMaxHandler(){



   this.templateXs=false
  this.templateSm=false
  this.templateMd=false
     this.templateMax=true


  this.$refs.templateWidth.classList.remove('tw-shadow-[0_0_2px_white]')

// this.$refs.templateWidth.classList.remove('tw-shadow-[0.5px_0.5px_3px_white]')

   this.$refs.templateWidth.classList.remove('tw-max-w-[900px]')
  this.$refs.templateWidth.classList.remove('tw-max-w-[1120px]')
  this.$refs.templateWidth.classList.remove('tw-max-w-[650px]')
this.$refs.templateWidth.classList.add('tw-max-w-[1170px]')


},

templateSizeReset() {
  this.$refs.templateWidth.classList.remove('tw-shadow-[0_0_2px_white]')

  //  this.$refs.templateWidth.classList.remove('tw-shadow-[0.5px_0.5px_3px_white]')
    //  this.$refs.templateWidth.classList.remove('tw-shadow-[0_0_2px_white]')


   this.$refs.templateWidth.classList.remove('tw-max-w-[900px]')
   this.$refs.templateWidth.classList.remove('tw-max-w-[1120px]')
   this.$refs.templateWidth.classList.remove('tw-max-w-[650px]')
   this.$refs.templateWidth.classList.add('tw-max-w-[1170px]')


 this.templateXs=false,
    this.templateSm=false,
    this.templateMd=false,
    this.templateMax=true
},

 clickHandler() {
            this.show=!this.show;
        },
        closePopup() {
          this.show=!this.show;
        },

        BulletVideoHandler(){
          this.bulletVideoVer=!this.bulletVideoVer;
          if(this.bulletVideoVer){

            this.$refs.variation.classList.remove('md:tw-flex-row')
            this.$refs.variation.classList.remove('md:tw-space-x-10')
          }
          if(!this.bulletVideoVer){
               this.$refs.variation.classList.add('md:tw-flex-row')
            this.$refs.variation.classList.add('md:tw-space-x-10')

          }

        }
    },

}



</script>

<style>

</style>