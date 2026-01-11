<!DOCTYPE html>
<html lang="gu">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Gujarati All-in-One AI App - Demo</title>
  <style>
    body { font-family: "Noto Sans Gujarati", Arial, sans-serif; background: #F6F8FB; margin:0; }
    header { background: #00695c; color: #fff; padding: 1.5rem; text-align: center; }
    main { padding: 2rem; }
    section { background: #fff; border-radius: 12px; padding: 1.5rem; margin-bottom: 2rem; box-shadow:0 2px 8px #0002; }
    h2 { color: #05786c; font-size: 1.3em; }
    input, button, textarea, select { font-size:1.1em; margin:0.5em 0; padding: 0.45em;}
    iframe { border:none; border-radius:12px; width:100%; }
    label { display:block; margin-top:0.5em; }
    textarea { width:100%; min-height:4em; }
    @media (max-width:600px) {
      main, section { padding:1em; }
      h1 { font-size: 1.25em;}
    }
  </style>
</head>
<body>
<header>
  <h1>ગુજરાતી All-in-One AI એપ - ડેમો</h1>
  <p>Speech, Photo Editing, Voice Change, Chat, Translation, Content - બધું એક જ જગ્યાએ!</p>
</header>
<main>
  <section>
    <h2>લખાણને અવાજમાં બદલો (Speech)</h2>
    <input id="gujtext" value="હેલો, તમારું સ્વાગત છે!">
    <button onclick="speakText()">અવાજમાં સાંભળો</button>
  </section>

  <section>
    <h2>બોલવાથી લખાણ (Speech to Text)</h2>
    <input id="gujresult" value="" placeholder="અહીં લખાણ આવશે">
    <button onclick="startRecognition()">બોલો</button>
  </section>

  <section>
    <h2>ફોટો એડિટિંગ/AI Photo Enhancer</h2>
    <iframe src="https://www.photopea.com/" height="400"></iframe>
    <br>
    <label>AI Photo Enhance માટે <a href="https://www.fotor.com/features/ai-photo-enhancer/" target="_blank">Fotor Enhancer</a> અથવા <a href="https://imglarger.com/" target="_blank">ImgLarger</a> વાપરો.</label>
  </section>

  <section>
    <h2>Photoમાંથી background કાઢી નાખો (Background Remover)</h2>
    <iframe src="https://www.remove.bg/upload" height="250"></iframe>
    <label>વૈકલ્પિક: <a href="https://cleanup.pictures/" target="_blank">Cleanup.pictures</a></label>
  </section>

  <section>
    <h2>Face Swap/Joke Maker/AI Avatar</h2>
    <iframe src="https://www.faceswapper.ai/" height="270"></iframe>
  </section>

  <section>
    <h2>AI Voice Changer (ગુજરાતી/Bollywood/Cartoon)</h2>
    <label>ઉપયોગ કરો: <a href="https://voicechanger.io/" target="_blank">VoiceChanger.io</a> | <a href="https://voicemaker.in/" target="_blank">Voicemaker.in</a></label>
  </section>
  
  <section>
    <h2>AI Chatbot/Language Assistant - Gujarati</h2>
    <iframe src="https://www.chatbase.co/chatbot-iframe/64b7a3dfdb379b000889e3c3" width="100%" height="420"></iframe>
  </section>

  <section>
    <h2>Document/Image Translator (Gujarati ↔ English)</h2>
    <label>Google Translate: <a href="https://translate.google.com/?sl=auto&tl=gu" target="_blank">Google Translate</a></label>
    <br>
    <label>Image Translate: <a href="https://translate.yandex.com/ocr" target="_blank">Yandex OCR Translate</a></label>
  </section>
  
  <section>
    <h2>Content Generator (AI લખાણ સહાયક)</h2>
    <textarea id="contentInput" placeholder="તમારો મુદ્દો લખો..."></textarea>
    <button onclick="generateContent()">AI શોધી આપે!</button>
    <textarea id="contentOutput" readonly placeholder="અહીં પરિણામ આવશે"></textarea>
    <label><small>ડેમો માટે ફક્ત JavaScript, API લગાવવી હોઈ શકે.</small></label>
  </section>

  <section>
    <h2>AI Video Editor</h2>
    <label>Free માટે: <a href="https://www.flexclip.com/tools/ai-video-editor.html" target="_blank">FlexClip</a> | <a href="https://clipchamp.com/en/ai-video-editor/" target="_blank">Clipchamp</a></label>
  </section>
</main>
<script>
function speakText() {
   var msg = new SpeechSynthesisUtterance();
   msg.text = document.getElementById("gujtext").value;
   msg.lang = "gu-IN";
   window.speechSynthesis.speak(msg);
}
function startRecognition() {
    const recognition = new (window.SpeechRecognition || window.webkitSpeechRecognition)();
    recognition.lang = "gu-IN";
    recognition.onresult = function(event) {
        document.getElementById('gujresult').value = event.results[0][0].transcript;
    }
    recognition.start();
}
// Demo Content Generator - API નહી, local alert/textarea
function generateContent() {
  var input = document.getElementById('contentInput').value;
  if(input.trim().length===0) {
    alert('મહેરબાની કરીને લખો...');
    return;
  }
  document.getElementById('contentOutput').value = "AI (ડેમો માટે):\n\"" + input + "\" વિષય પર AI લખાણ અહીં આવશે.";
}
</script>
</body>
</html>
# Gujarati AI Teacher

Gujarati AI Teacher એ Gujarati ભાષામાં બનાવેલું AI આધારિત શિક્ષણ એપ છે.

## Features
- ધોરણ 1 થી 12 માટે મદદ
- Gujarati ભાષામાં પ્રશ્ન-જવાબ
- સરળ અને ઝડપી ઉપયોગ
- ભવિષ્યમાં AI + Ads દ્વારા આવક

## Live App
Website link જલ્દી ઉપલબ્ધ થશે.

## Developer
Mitul Thakor
