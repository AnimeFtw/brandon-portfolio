<template>
  <div class="flex flex-col gap-[2.5rem]">
    <!-- introduction section -->
    <div class="divCenter">
      <p
        id="landing_intro"
        ref="landingIntro"
        class="lg:text-xl text-md acrlyic w-auto text-center selector"
      ></p>
    </div>
    <section class="">
      <h1 class="text-4xl font-bold">Brandon Santis</h1>
      <h3 class="text-lg">Professional Full Stack Web Developer</h3>
    </section>
    <section class="pt-2">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Professional background
      </h2>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        &nbsp;&nbsp;&nbsp;&nbsp; Professional web developer capable professional
        looking and user-friendly websites from scratch and writes
        <strong>performance optimized, reusable and refactorable codes</strong>.
        Professionally developed web applications with multiple Javascript
        frameworks.
      </p>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        <!-- &nbsp;&nbsp;&nbsp;&nbsp; -->
        Hungry for knowledge, collaborative individual and possess analytical
        skills. Enjoys problem solving and willing to adapt to changes in the
        industry to stay on top.
      </p>
    </section>
    <!-- info section -->
    <section class="">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Bio
      </h2>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        &nbsp;&nbsp;&nbsp;&nbsp; I have a strong passion on technology and
        computers. I initially went to Pennsylvania College of Technology to
        pursue my degree in Electronics and Computer Engineering
        Technology-Robotics and Automation Emphasis. One of the classes I took
        in college that stuck out to me was Introduction To Microprocessors
        where I learned how to code Zybo boards using the C programming language
        and making the little leds light up in in different sequences depending
        on the analog input. When I graduated college I realized what I studied
        for was not something I wanted to do so I decided to pursue a different
        career path. I really wanted to get into coding and I became really
        interested in web development. Outside of programmimg, I have have a
        hobby of learning and engagement with technology. I like to tinker with
        my Arch Linux Operating System while also using it as my daily driver
        and enjoy building PCs for people while teaching them about Linux.
      </p>
    </section>
    <!-- journey section -->
    <section class="">
      <h2
        class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2"
      >
        Journey
      </h2>
      <br />
      <div class="flex flex-col gap-2">
        <!-- year 2017 -->
        <p class="lg:text-lg text-sm text-justify">
          <strong>2014-2019:</strong>
          &nbsp; Enrolled at Pennsylvania College of Technology for my Robotics
          and Automation Degree.
        </p>
        <!-- year 2020 -->
        <p class="lg:text-lg text-sm text-justify">
          <strong>2022:</strong>
          Decided to change my career choice to web development as I grew very
          interested in programming.
        </p>
        <!-- year 2022  -->
      </div>
    </section>
  </div>
</template>

<script>
  import TypeIt from 'typeit';
  import 'animate.css';
  import { ref } from 'vue';

  export default {
    data() {
      return {
        display: false
      };
    },
    setup() {
      const landingIntro = ref('');

      if (landingIntro.value !== '') {
        landingIntro.value === '';
      }
    },
    mounted() {
      new TypeIt('#landing_intro', {
        speed: 50,
        waitUntilVisible: true,
        startDelay: 2000,
        startDelete: true,
        // remove cursor when finished
        afterComplete: function (instance) {
          instance.destroy();
        }
      })
        .type('Hello! I am a full stack web developer based in Pennsylvania!')
        .go();
    }
  };
</script>

<style>
  .selector {
    background-color: var(--bg-sel);
  }

  .copyright {
    animation: fadeInLeft; /* referring directly to the animation's @keyframe declaration */
    animation-duration: 1s; /* don't forget to set a duration! */
    animation-delay: 3s;
  }

  /* @keyframes copyright {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
    visibility: visible;
  }
} */
</style>
