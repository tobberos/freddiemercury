---
layout : default
---
<div class="center-text">
<h1>Freddie Mercury</h1>
<p class="quoteText">"I wont be a rockstar. I will be a legend."</p>
</div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/animejs/2.0.2/anime.min.js"></script>
<script>
var textWrapper = document.querySelector('.quoteText');
textWrapper.innerHTML = textWrapper.textContent.replace(/\S/g, "<span class='letter'>$&</span>");
anime({
    targets: '.quoteText .letter',
    scale: [4,1],
    opacity: [0,1],
    translateZ: 0,
    easing: "easeOutExpo",
    duration: 950,
    delay: (el, i) => 70*i
  });
</script>