<template>
<div class="tw-w-5 tw-h-5 tw-rotate-45  tw-bg-black"></div>
  <!-- <div @click.self="hideScreen()" class=" bg-[#2D2D2D] relative  mx-auto  items-center   overflow-x-hidden min-h-screen ">

    <div
      class="mx-auto max-w-[1170px] py-7   rounded-sm md:mt-4  relative z-10    items-center justify-center     ">


      <div
        class=" md:p-0 lg:px-10 bg-transparent w-full px-1 flex flex-col items-center pt-5 md:py-0 relative z-[3] md:top-auto mx-auto  text-center  ">

        <div class="border border-orange-300 relative w-full ">
          <button
            class="items-center py-1 absolute bottom-[100%]  right-0 text-white bg-orange-300  flex justify-end px-2 rounded-t-md">
            <span class="material-icons text-white">
              settings
            </span>
          </button>
          <p
            class=" mx-auto text-center mb-5 px-1 font-normal text-base md:text-2xl lg:text-[28px] text-[#fbfbfb]  subheading w-fit  ">
         {{subheading}}
          </p>
        </div>

        <div class="border border-orange-300 relative w-full ">
          <button
            class="items-center py-1 absolute bottom-[100%]  right-0 text-white bg-orange-300  flex justify-end px-2 rounded-t-md">
            <span class="material-icons text-white">
              settings
            </span>
          </button>
          <h2 ref="heading-text"
            class="text-2xl {{}} md:text-4xl lg:text-[58px] md:leading-[1.1]   mb-4 text-center  heading font-bold text-transparent bg-clip-text bg-gradient-to-r  from-[#fb01b4] via-[#d278d3] to-[#1dffe1] tracking-[-1px] bg-[radial-gradient(circle at 0px 0px, #ff61d3 25%, #b318ff 45%, #00f0ff 65%, #3cf7a2 85%);] ">
{{headingData}}

          </h2>
        </div>

        <div class="border border-orange-300 relative w-full ">
          <button
            class="items-center py-1 absolute bottom-[100%]  right-0 text-white bg-orange-300  flex justify-end px-2 rounded-t-md">
            <span class="material-icons text-white">
              settings
            </span>
          </button>

          <p class="  text-sm md:text-xl lg:text-2xl     call  text-[#ffffff]  ">
            Call To Action Statement Goes Here!</p>

        </div>



        <form action=""
          class="flex flex-col md:px-5 justify-center w-full px-1 md:w-[95%] space-y-6  rounded-md  mb-2 mt-4  items-center ">

          <div class="border border-orange-300 relative w-full ">
            <button
              class="items-center py-1 absolute bottom-[100%]  right-0 text-white bg-orange-300  flex justify-end px-2 rounded-t-md">
              <span class="material-icons text-white">
                settings
              </span>
            </button>
            <input  type="email" placeholder="Your Email Address Here ..."
              class="outline-none border focus:border-[#921dbd] rounded-md w-full lg:w-[80%]  shadow-sm text-black   px-4 py-3 ">

          </div>

          <div class="group ">
            <div class="border border-orange-300 relative w-full ">
              <button
                class="items-center py-1 absolute bottom-[100%]  right-0 text-white bg-orange-300  flex justify-end px-2 rounded-t-md">
                <span class="material-icons text-white">
                  settings
                </span>
              </button>
              <button
:class="showButton && 'bg-green-200' "
                class="cursor-pointer bg-[#6438F8] hover:bg-[#704edf]  text-white border-8 border-transparent  font-bold   hover:animate-none  py-2 md:py-4 md:px-4 md:text-4xl w-full md:w-fit flex btn space-x-2 md:space-x-4  justify-center items-center transition-all sm:group-hover:-translate-y-3 sm:group-hover:px-10  ease-in-out text-2xl rounded-full " >

                <p class="">GET INSTANT ACCESS NOW!</p>

              </button>

            </div>
          </div>

          <div class="border border-orange-300 relative w-full ">
            <button
              class="items-center py-1 absolute bottom-[100%]  right-0 text-white bg-orange-300  flex justify-end px-2 rounded-t-md">
              <span class="material-icons text-white">
                settings
              </span>
            </button>
            <p
              class=" align-baseline text-xs md:text-sm text-center font-medium disclaimer text-[#fdfdfd] ">
              We respect
              your
              privacy,
              Your
              email
              address will
              never be
              shared or sold</p>


          </div>
        </form>

      </div>

    </div>

    <div v-if="secondTemplate" class="bg-green-100 w-full flex justify-center items-center min-h-[300px]">

<slot>

</slot>

    </div>
<div class="absolute bottom-44 left-[50%] translate-x-[-50%] max-w-3xl space-y-2 flex flex-col items-center">
<input type="text" class="outline-none py-2 px-4 w-full" placeholder="write text" ref="headingValue" >
<button @click="e=>{
  changeHeading();
  toogleButton();
}"  class="px-4 py-2 rounded-md bg-purple-200 ">Teading Text</button>
</div>
  </div> -->
</template>



<script>




export default {
  name: 'Template',
  props: {
    msg: String,
    heading:String,
    subheading:String,
    secondTemplate:Boolean,

  },
  data(){
    return {
headingData:'this is from data',
color:'hidden',
hide:false,
showButton:false,
    }
  },
  methods: {
       toogleButton(e) {
 this.showButton=!this.showButton;
    },
    changeHeading(e) {
      this.headingData=this.$refs.headingValue.value;
      this.color=!this.color;
    },
hideScreen() {
  this.$emit('close')
}


  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

