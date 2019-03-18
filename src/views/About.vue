<template>
<div>

  <div class="about">
    <h1>This is an about page</h1>
    <input type="text" v-model="inputField">
    <button @click="call">call</button>
  </div>
</div>

</template>
<script>
// @ is an alias to /src
import axios from 'axios';
import moment from 'moment';
import jsPDF from 'jspdf';
import html2canvas from 'html2canvas'
// import hummus from 'hummus'

export default {
  name: 'home',
  data() {
    return {
      inputField: ''
    }
  },

  methods: {
    call() {
      html2canvas(document.getElementById('toRender')).then(canvas => {
        var img = canvas.toDataURL("image/png");
          var doc = new jsPDF();
          doc.addImage(img, 'JPEG', -80,0);
          doc.save('test.pdf')
      }) 
       
  
        
   
      // var self = this
      // var doc = new jsPDF();
      // doc.text(20,20, self.inputField)
      // doc.addPage();
      // doc.text(20,20,self.inputField)
      // doc.save('test.pdf')
    }
  }

}

   




</script>
<style>
/* #toRender {
  width: 100%;
  height: 100%;
} */

/* #toRender img {
  width: 100%;
} */
</style>
