<template>
  <div id="video" class=" tw-group tw-p-1  tw-border-gray-500 tw-w-full tw-text-center tw-mb-4 ">

          <iframe

          ref="video"
          :class="full && templateXs ? 'md:tw-h-[295px] md:tw-w-[525px]' : max ? 'md:tw-max-w-[807px] md:tw-h-[454px]' : full ? 'md:tw-max-w-[807px] md:tw-h-[454px] ' : 'md:tw-h-[295px] md:tw-w-[525px]' "
           class=" tw-aspect-video md:tw-aspect-auto tw-w-full  tw-mx-auto tw-rounded-sm  "
            src="https://www.youtube.com/embed/tf88GFLtj18?autoplay=0&amp;controls=0&amp;showinfo=0&amp;title=0&amp;rel=0&amp;wmode=transparent"
            allowtransparency="true" frameborder="0" scrolling="no" allowfullscreen="allowfullscreen"
            mozallowfullscreen="mozallowfullscreen" webkitallowfullscreen="webkitallowfullscreen"
            oallowfullscreen="oallowfullscreen" msallowfullscreen="msallowfullscreen" id="" wmode="opaque"></iframe>



        <div v-if="!videoDescription && !full && !max" class="tw-text-white tw-text-sm tw-mt-3 md:tw-mt-3 tw-mx-auto" :class="onlyVideo && 'md:!tw-w-[65%]'">
            <p :class="bulletVideoVer && 'md:tw-w-[65%] tw-mx-auto'" class="fonts-lato  ">Robert Syslo Jr. is the founder of a 7 figure creative agency called Syslo Ventures, has 18+ years experience building the worlds largest brands, and has been featured on Yahoo Finance, Fox News, and USA Today as one of the Top Business Leaders to Follow for Promotion and Marketing!</p>
        </div>

        </div>
</template>

        <!-- :class="full || max ? 'md:tw-max-w-[807px] md:tw-h-[454px] tw-px-1' :'md:tw-h-[295px] md:tw-w-[525px]'" -->

  <!-- <div id="video" class=" tw-group tw-p-1  tw-border-gray-500 tw-w-full tw-text-center tw-mb-4 ">

          <iframe
          ref="video"
          :class="onlyVideo ? 'md:tw-w-[807px] md:tw-h-[454px]' :bulletVideoVer ? 'md:tw-w-[807px] md:tw-h-[454px]' :' md:tw-h-[295px] md:tw-w-[525px]'"
           class=" tw-aspect-video md:tw-aspect-auto tw-w-full  tw-mx-auto tw-rounded-sm  "
            src="https://www.youtube.com/embed/tf88GFLtj18?autoplay=0&amp;controls=0&amp;showinfo=0&amp;title=0&amp;rel=0&amp;wmode=transparent"
            allowtransparency="true" frameborder="0" scrolling="no" allowfullscreen="allowfullscreen"
            mozallowfullscreen="mozallowfullscreen" webkitallowfullscreen="webkitallowfullscreen"
            oallowfullscreen="oallowfullscreen" msallowfullscreen="msallowfullscreen" id="" wmode="opaque"></iframe>

<div v-if="!videoDescription" class="tw-text-white tw-text-sm tw-mt-3 md:tw-mt-3 tw-mx-auto"  :class="onlyVideo && 'md:!tw-w-[65%]'">
  <p :class="bulletVideoVer && 'md:tw-w-[65%] tw-mx-auto'" class="fonts-lato">Robert Syslo Jr. is the founder of a 7 figure creative agency called Syslo Ventures, has 18+ years experience building the worlds largest brands, and has been featured on Yahoo Finance, Fox News, and USA Today as one of the Top Business Leaders to Follow for Promotion and Marketing!</p>
</div>

        </div> -->

<script>


export default {
name:'Video',
props:{
  onlyVideo:false,
  videoDescription:false,
  bulletVideoVer:false,
  full:false,
  max:false,
  templateXs:false

},
methods:{
//   checkVer(){
// if(this.bulletVideoVer){
// this.$refs.video.classList.remove('md:tw-h-[295px] ')
// this.$refs.video.classList.remove('md:tw-w-[525px]')
// // this.$refs.video.classList.add('md:!tw-w-[807px],md:!tw-h-[454px]')

// console.log(this.$refs.video,this.bulletVideoVer)
// }
// // if(!this.bulletVideoVer){
// // this.$refs.video.classList.add('md:tw-h-[295px] md:tw-w-[525px]')
// // }
//   }
}
}
</script>

<style>

</style>