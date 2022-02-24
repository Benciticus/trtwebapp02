<template>
<div class="wrapper">
  <div class="vertical panel1">
    <WinChoices/>
    <WinFootnotes/>
  </div>
  <div class="vertical panel2">
    <WinExtract/>
  </div>
</div>
</template>

<script>
import Phrase from './components/Phrase.vue'
import WinChoices from './components/WinChoices.vue'
import WinFootnotes from './components/WinFootnotes.vue'
import WinExtract from './components/WinExtract.vue'

export default {
  name: 'App',
  components: {
    Phrase,
    WinChoices,
    WinFootnotes,
    WinExtract,
    WinChoices
  },
  data(){
    
  }
}
</script>

<style>
html, body{
  overflow: hidden;
}
body{
  font-family: arial;
  background: #ffffff;
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
a, p {
  margin:0;
  padding:0
}
.wrapper{
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}
.wrapper > div {
  flex: 1 1;
}
.wrapper_tbx {
  padding: 20px;
}
.box{
  border: #ddd;
  display: inline-block;
  height: 100%;
  width: 100%
}
.hidden{
  display: none;
}
.vertical.panel1{
  width: 80vw;
}
.vertical.panel2{
  width: 20vw;
}
.horizontal.panel1{
  height: 66vh;
}
.horizontal.panel2{
  height: 34vw;
}
.main_textbox{
  width: 100%;
  height: 100%;
  resize: none;
  font-family: Arial, Helvetica, sans-serif;
  border: #727272;
}
.windowChoices {
  line-height: 1.75em;
}
.windowFootnotes {

}
.windowExtract {

}
.highlighted{
  background-color: #c4c4c4
}
.highlighted.choice{
  background-color: #9dcbff
}
.chapTitle{
  font-style: bold;
  font-size: 3em;
}
.chapSubtitle{
  font-style: bold;
  font-size: 2em;
}
.chapNum{
  font-style: bold;
  font-size: 3.5em;
}
.secNum{
  font-style: italic;
  font-size: 1.25em;
}
.secTitle{
  font-style: bold;
  font-size: 1.25em;
}
.subsecNum{
  font-style: italic;
  font-size: 1.00em;
}
.subsecTitle{
  font-style: bold;
  font-size: 1.00em;
}
.secParallel{
  font-style: italic;
  font-size: 1em;
}
.curly, .vNum{
  font-weight: bold;
}
.fNum{
  font-weight: bold;
  vertical-align: super;
  font-size: .65em;
  color: #e237b7;
}
.super{
  font-style: italic;
  vertical-align: super;
  font-size: .65em;
}
</style>
