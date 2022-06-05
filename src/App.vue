<script setup>
import ThreeJS from './components/ThreeJs.vue'
import Footer from './components/Footer.vue'
import Navbar from './components/Navbar.vue'
import 'animate.css'
</script>

<template>
<div class="3xl:px-[5rem] 4xl:px-[10rem] 5xl:px-[20rem] 6xl:px-[50rem] 7xl:px-[100rem] 8xl:px-[150rem]">
  <div class="xl:px-[20rem] lg:px-[14rem] md:px-[10rem] sm:px-[7rem] px-[2rem] overflow-hidden ">
    <Navbar />
    <ThreeJS />
    <div class="pb-20 z-10 -mt-[5rem]">
      <!-- contents -->
      <router-view v-slot="{ Component }">
        <transition 
        mode="out-in"
        enter-active-class="animate__animated animate__fadeInUp animate__fast"
        leave-active-class="animate__animated animate__fadeOutDown animate__fast"
        >
          <component :is="Component" />
        </transition>
      </router-view>
    </div>
  </div>
</div>
</template>

<style>
:root {
	--white: #ffffff;
  --whiteFilter: invert(100%) sepia(0%) saturate(7482%) hue-rotate(149deg) brightness(101%) contrast(100%);
  --gray0: #f8f8f8;
  --gray1: #eeeeee;
  --gray2: #dcdcdc;
  --oxfordBlue: #011936;
  --oxfordBlueFilter: invert(6%) sepia(27%) saturate(6747%) hue-rotate(203deg) brightness(96%) contrast(99%);
  --blackCoral: #465362;
  --morningBlue: #82A3A1;

  --gray8: #2d2d2d;
  --gray8T: #2d2d2dee;
  --gray9: #232323;
  --gray10: #161616;

  --cyan1: #D8FDF7;
  --cyan2: #C5FCF3;
  --cyan2T: #b1fbefee;
  --cyan3: #B1FBEF;
  --cyan4: #9EFAEB;
  --cyan5: #64F7DE;
  --cyan6: #2AF4D2;
  --cyan7: #0BD5B4;

  /* dark mode */

  /* solarized mode */
  --solar1: #002b36;
  --solar2: #073642;
  --solar2T:#073642ee;
  --solar3: #586e75;
  --solar4: #657b83;
  --solar5: #839496;
  --solar6: #93a1a1;
  --solar7: #eee8d5;
  --solar8: #fdf6e3;
  --solar8T: #fdf6e3ee;
  --solar9: #b58900;
  --solar10: #859900;
  --solar11: #2aa198;
  --solar12: #084a47;
  --solar11Filter: invert(50%) sepia(82%) saturate(361%) hue-rotate(126deg) brightness(91%) contrast(89%);

  /* starfall  */
  --starfall-bg: #1b2636;
  --starfall-text: #cacde2;
  --starfall-sel: #214d63ee;
  --starfall-highlight: #e278c4;
  --starfall2: #8de8b0;
}

@media (max-width: 370px) {
  html, body {
    overflow:hidden;
    position: absolute;
  }
}

body {
	background-color: rgb(45, 45, 45);
  font-family: Helvetica, Roboto, sans-serif;
  color: var(--text);
  caret-color: var(--text);
  background-color: var(--bg);
  transition: background 500ms ease-in-out, color 1000ms ease-in-out, filter 2000ms ease-in-out;
  
}

.divCenter {
  display: flex;
  align-items: center;
  justify-content: center;
}

.light {
  --bg: var(--cyan1); 
  --bg-sel: var(--cyan2T);
  --svg-color: var(--oxfordBlueFilter);
  --text: var(--oxfordBlue);
  --ti-cursor-color: var(--text);
  --text-highlight: var(--solar2);
  --text-highlight-2: var(--starfall-highlight);
}

.dark {
  --bg: var(--gray9);
  --bg-sel: var(--gray8T);
  --svg-color: var(--whiteFilter);
  --text: var(--white);
  --ti-cursor-color: var(--text);
  --text-highlight: var(--cyan3);
  --text-highlight-2: var(--starfall-highlight);
}

.solarized {
  --bg: var(--solar8);
  --bg-sel: var(--solar8T);
  --svg-color: var(--oxfordBlueFilter);
  --text: var(--solar12);
  --ti-cursor-color: var(--text);
  --text-highlight: var(--solar11);
  --text-highlight-2: var(--solar9);
}

.dark_solar {
  --bg: var(--solar1);
  --bg-sel: var(--solar2T);
  --svg-color: var(--solar11Filter);
  --text: var(--solar11);
  --ti-cursor-color: var(--text);
  --text-highlight: var(--solar10);
  --text-highlight-2: var(--solar10);
}

.starfall {
  --bg: var(--starfall-bg);
  --bg-sel: var(--starfall-sel);
  --svg-color: var(--whiteFilter);
  --text: var(--starfall-text);
  --ti-cursor-color: var(--text); 
  --text-highlight: var(--starfall-highlight);
  --text-highlight-2: var(--starfall2);
}

.acrlyic {
  -webkit-backdrop-filter: blur(20px) saturate(180%);
  backdrop-filter: blur(20px) saturate(180%);
  padding: 1rem 2rem;
  border-radius: 4px;
  box-shadow: 0 4px 12px 0 rgba(0, 0, 0, 0.1);
}

h2 {
  color: var(--text-highlight);
}

strong {
  color: var(--text-highlight-2);
}
</style>

