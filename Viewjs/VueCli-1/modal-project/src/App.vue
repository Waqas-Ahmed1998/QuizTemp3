<template>
<!-- <div class=" tw-bg-black tw-max-w-5xl tw-mx-auto tw-p-10"> -->
 <!-- <QuizForma1Vue/> -->
<!-- <QuizFormaTemplate2Vue/> -->
<!-- <QuizFormaBaseTemplateVue/> -->
<!-- <QuizTemp2Vue/> -->
<QuizTemp3Vue/>
<!-- <WidgetVue/> -->
<!-- <MockupEditorVue/> -->
<!-- </div> -->
<!-- <TemplateVue/> -->
<!-- <Template1Vue/> -->
</template>

<script>

import WidgetVue from './components/Widget.vue'
import TemplateVue from './components/Template.vue'
import Template1Vue from './components/Template-1.vue'
import MockupEditorVue from './components/MockupEditor.vue'
import QuizForma1Vue from './components/QuizForma1.vue'
import QuizFormaTemplate2Vue from './components/QuizFormaTemplates/QuizFormaTemplate2.vue'
import  QuizFormaBaseTemplateVue from './components/QuizFormaTemplates/QuizFormaBaseTemplate.vue'
import QuizTemp2Vue from './components/QuizFormaTemplates/QuizTemp2.vue'
import QuizTemp3Vue from './components/QuizFormaTemplates/QuizTemp3.vue'
import './assets/tailwind.css'

export default {
  name: 'App',
  components: {
    TemplateVue,
Template1Vue,
WidgetVue,
MockupEditorVue,
QuizForma1Vue,
QuizFormaTemplate2Vue,
QuizFormaBaseTemplateVue,
QuizTemp2Vue,
QuizTemp3Vue

},
data(){
  return {
secondTemplate:false,
    showScreen:true,
    showScreen2:false
  }
},
  methods:{
    changeText(){
this.$refs.heading.classList.toggle('bg-black')
this.$refs.checkboxx.checked=!this.$refs.checkboxx.checked
    },
    toggleScreen() {
this.showScreen=!this.showScreen
    },
    toggleScreen2() {
this.showScreen2=!this.showScreen2
this.secondTemplate=!this.secondTemplate
    }

  }
}
</script>


