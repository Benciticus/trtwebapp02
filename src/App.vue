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
    return{
      items: [
        {choice: false, lvl: 1, type: 'vNum', id:1, isHighlighted: true, content: '1 ', subitems: NaN},
        {choice: false, lvl: 1, type: 'DI', id:2, isHighlighted: true, content: 'DI ', subitems: NaN},
        {choice: false, lvl: 1, type: 'fNum', id:3, isHighlighted: true, content: '06', subitems: NaN},        
        {choice: false, lvl: 2, type: 'curlOpen', id:4, isHighlighted: false, content: '{', subitems: NaN},
        {choice: false, lvl: 2, type: 'contents', id:4, isHighlighted:false, content: '',
          subitems: [
            {choice: false, lvl: 2, type: 'contents', id:4, isHighlighted:false, content: '',
              subitems: [
                {choice: true, lvl: 3, type: 'pareOpen', id:5, isHighlighted: false, content: '(', subitems: NaN},
                {choice: true, lvl: 3, type: 'contents', id:4, isHighlighted:false, content: '',
                  subitems: [
                    {choice: true, lvl: 4, type: 'phr', id:6, isHighlighted: false, content: 'This is the'},
                  ]
                },
                {choice: true, lvl: 3, type: 'pareClos', id:7, isHighlighted: false, content: ')'},
                {choice: true, lvl: 2, type: 'phr', id:8, isHighlighted: true, content: ' beginning of the gospel '},        
                {choice: false, lvl: 2, type: 'contents', id:4, isHighlighted:false, content: '',
                  subitems: [
                    {choice: true, lvl: 3, type: 'word1', id:9, isHighlighted: true, content: 'of'},
                    {choice: false, lvl: 3, type: 'fwdSlash', id:10, isHighlighted: false, content: '/'},
                    {choice: true, lvl: 3, type: 'word2', id:11, isHighlighted: false, content: 'about '}
                  ]
                },
                {choice: true, lvl: 2, type: 'phr', id:12, isHighlighted: true, content: 'Jesus '},
                {choice: false, lvl: 2, type: 'DI', id:13, isHighlighted: true, content: 'DI '},
                {choice: false, lvl: 2, type: 'fNum', id:14, isHighlighted: true, content: '07'},
                {choice: true, lvl: 2, type: 'phr', id:15, isHighlighted: true, content: 'Christ, '},
                {choice: false, lvl: 2, type: 'fNum', id:16, isHighlighted: true, content: '08'},
                {choice: true, lvl: 3, type: 'squaOpen', id:17, isHighlighted: true, content: '['},
                {choice: true, lvl: 4, type: 'pareOpen', id:18, isHighlighted: false, content: '('},
                {choice: false, lvl: 2, type: 'contents', id:4, isHighlighted:false, content: '',
                  subitems: [
                    {choice: true, lvl: 4, type: 'phr', id:19, isHighlighted: false, content: 'the'}
                  ]
                },
                {choice: true, lvl: 4, type: 'pareClos', id:13, isHighlighted: false, content: ')'},
                {choice: true, lvl: 3, type: 'phr', id:14, isHighlighted: true, content: ' Son of God'},
                {choice: true, lvl: 3, type: 'squaClos', id:20, isHighlighted: true, content: ']'},
                {choice: true, lvl: 2, type: 'phr', id:21, isHighlighted: true, content: ': '},
              ],
            },
            {choice: false, lvl: 2, type: 'phr', id:22, isHighlighted: false, content: '⇔'},
            {choice: false, lvl: 2, type: 'contents', id:4, isHighlighted:false, content: '',
              subitems: [
                {choice: true, lvl: 2, type: 'phr', id:23, isHighlighted: false, content: ' The good '},
                {choice: false, lvl: 2, type: 'contents', id:4, isHighlighted:false, content: '',
                  subitems: [
                    {choice: true, lvl: 3, type: 'word1', id:9, isHighlighted: true, content: 'message'},
                    {choice: false, lvl: 3, type: 'fwdSlash', id:10, isHighlighted: false, content: '/'},
                    {choice: true, lvl: 3, type: 'word2', id:11, isHighlighted: false, content: 'news'}
                  ]
                },
                {choice: true, lvl: 2, type: 'phr', id:27, isHighlighted: false, content: 'about '},
                {choice: true, lvl: 3, type: 'squaOpen', id:28, isHighlighted: false, content: '['},
                {choice: false, lvl: 2, type: 'contents', id:4, isHighlighted:false, content: '',
                  subitems: [
                    {choice: true, lvl: 3, type: 'phr', id:28, isHighlighted: false, content: "God's Son"},
                  ]
                },
                {choice: true, lvl: 3, type: 'squaClos', id:28, isHighlighted: false, content: ']'},
                {choice: true, lvl: 2, type: 'phr', id:28, isHighlighted: false, content: ' Jesus '},
                {choice: false, lvl: 2, type: 'DI', id:28, isHighlighted: false, content: 'DI'},
                {choice: true, lvl: 2, type: 'phr', id:28, isHighlighted: false, content: ' Christ begins'}
              ]
            },
          ]
        },
        {choice: false, lvl: 2, type: 'curlClos', id:28, isHighlighted: false, content: '}'}
      ]
    }
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
