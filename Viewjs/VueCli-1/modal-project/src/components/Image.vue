<template>
  <div :class="max && templateMd && 'md:tw-scale-[0.9]'" class="  tw-flex tw-flex-col">
   <img src="../assets/maxPicture.png" alt="" :class="templateSm && max && 'md:tw-max-w-[585px] tw-mx-auto'" class="md:tw-max-w-[585px] md:tw-h-[370px] tw-object-containt md:tw-object-contain">
<p :class="templateSm && max && 'md:tw-max-w-[585px] tw-mx-auto '" class="tw-py-2 tw-text-xs md:tw-text-sm tw-text-center tw-text-white tw-mb-2">figure creative agency called Syslo Ventures, has 18+ years experience building the worlds largest brands, and has been featured on Yahoo Finance, Fox News, and USA Today as one of the Top Business Leaders to Follow for Promotion and Marketing!</p>
  </div>
</template>

<script>
export default {
name:'Image',
props:['max','templateSm','templateMd']

}
</script>

<style>

</style>