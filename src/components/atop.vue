<template>
    <div class="tposition">
        <div class="txt">
            <a class="codepen-button"><span>
                Hey there! 🌟 I couldn't help but notice your amazing vibe and just had to say hi. 😊 Your smile is like sunshine on a cloudy day, and I'd love to get to know you better. 💬 What do you say we start a conversation and see where it goes? 🌹
                by the way??.... Jii🥰🤗. I'm Satya. I was too querious to talk with but i was confused then i think to create this app for YOU---> let us be Friends.... </span></a>
        </div>
        <div class="3dmodle">
            <img src="../assets/images/gojo.jpeg" alt="knowtogether">
        </div>
    </div>
</template>



<style scoped>
.tposition{
    display: grid;
    grid-template-columns: 60% 20%;
    gap: 10%;
    text-align: left;
    padding: 10px;
}

img{
    width: auto;
    height: auto;
    border-radius: 20%;
    box-shadow: 10px 10px 10px rgba(205, 21, 144, 0.855);
}



/* From Uiverse.io by SelfMadeSystem */ 
/* Yoinked from CodePen, but improved the animation
so that it is smooth among other more minor things */

.codepen-button {
  display: block;
  cursor: pointer;
  color: white;
  margin: 0 auto;
  position: relative;
  text-decoration: none;
  font-weight: 600;
  border-radius: 6px;
  overflow: hidden;
  padding: 3px;
  isolation: isolate;
}

.codepen-button::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 400%;
  height: 100%;
  background: linear-gradient(115deg,#4fcf70,#fad648,#a767e5,#12bcfe,#44ce7b);
  background-size: 25% 100%;
  animation: an-at-keyframe-css-at-rule-that-translates-via-the-transform-property-the-background-by-negative-25-percent-of-its-width-so-that-it-gives-a-nice-border-animation_-We-use-the-translate-property-to-have-a-nice-transition-so-it_s-not-a-jerk-of-a-start-or-stop .75s linear infinite;
  animation-play-state: paused;
  translate: -5% 0%;
  transition: translate 0.25s ease-out;
}

.codepen-button:hover::before {
  animation-play-state: running;
  transition-duration: 0.75s;
  translate: 0% 0%;
}

@keyframes an-at-keyframe-css-at-rule-that-translates-via-the-transform-property-the-background-by-negative-25-percent-of-its-width-so-that-it-gives-a-nice-border-animation_-We-use-the-translate-property-to-have-a-nice-transition-so-it_s-not-a-jerk-of-a-start-or-stop {
  to {
    transform: translateX(-25%);
  }
}

.codepen-button span {
  position: relative;
  display: block;
  padding: 1rem 1.5rem;
  font-size: 1.1rem;
  background: #d5cbcbdd;
  border-radius: 3px;
  height: 100%;
}

@media screen and (max-width:446px) {
  .tposition{
    grid-template-columns: none;
    grid-template-rows:auto;
    text-align: center;
    padding: 5% 0 0 0%;
}
}
</style>