<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
//import AmiriRegular from './assets/Amiri-Regular.ttf'
//import  AmiriFont  from './amiri_font.js'
import { jsPDF } from "jspdf";



// Default export is a4 paper, portrait, using millimeters for units
const pdf = new jsPDF();
// pdf.addFileToVFS('Amiri-Regular.ttf', AmiriFont.font);
// pdf.addFont('Amiri-Regular.ttf', 'Amiri-Regular', 'normal');
// pdf.setFont("Amiri-Regular");
//
//
// //doc.text("السلام عليكم", 10, 10,{lang: "ar"});
//
// pdf.html(document.getElementById('html-print'), {
//     callback: function (pdf) {
//         window.open(pdf.output('bloburl'));
//         //pdf.save('a4.pdf');
//     },
//     lang: "ar"
// });

const AmiriRegular = pdf.loadFile("https://rawcdn.githack.com/MrRio/jsPDF/cbc85b4bb66d5c1a2d50d199e8bf33836f2f12d7/test/reference/Amiri-Regular.ttf", true);
pdf.addFileToVFS("Amiri-Regular.ttf", AmiriRegular);

pdf.addFont("Amiri-Regular.ttf", "Amiri", "normal");
pdf.html(document.getElementById('html-print'), {
    callback: function (pdf) {
        window.open(pdf.output('bloburl'));
        /*var iframe = document.createElement('iframe');
        iframe.setAttribute('style', 'position:absolute;top:0;right:0;height:100%; width:600px');
        document.body.appendChild(iframe);
        iframe.src = pdf.output('datauristring');*/
    }
});

//doc.save("a4.pdf");
export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
