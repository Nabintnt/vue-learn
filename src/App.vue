<template>
   <div>
    <h1>{{ message }}</h1>
    <button @click="count++">{{ count }}</button>
    <div v-html="rawHtml"></div>
    {{rawHtml}}

    <p  :style="myStyle">
      This is red
    </p>

    <p  v-if="paragraphShow">This is not hidden</p>
    <p v-else>This is hidden</p>

    <button @click="this.paragraphShow = !this.paragraphShow">Toggle</button>



  <div>
    <label for="">
      <button @click="this.charShow = 'A'">A</button>
      <button @click="this.charShow = 'B'">B</button>
      <button @click="this.charShow = 'C'">C</button>
      <button @click="this.charShow = ''">Else</button>
    </label>
  </div>

  <div v-if="charShow === 'A'">
    A
  </div>
  <div v-else-if="charShow === 'B'">
    B
  </div>
  <div v-else-if="charShow === 'C'">
    C
  </div>
  <div v-else>
    Not A/B/C
  </div>


   </div>
</template> 
<script>
export default {
  beforeMount(){
    // alert("Click Me To Open 😍 ");
  },
  data() {
    return {
      charShow : "A",
      paragraphShow:true,
      message:"Wel come to Vue Tutorial",
      count: 0,
      rawHtml:"<h1>This is for test</h1>",
      myStyle:{
        'background-color':'red',
      }
    }
  },
}
</script>
<style scoped>

</style>
