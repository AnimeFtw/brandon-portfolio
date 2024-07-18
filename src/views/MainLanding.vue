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
        &nbsp;&nbsp;&nbsp;&nbsp; Enthusiastic front-end developer with hands-on
        experience in both front-end and back-end development. Proficient in
        HTML5, CSS3, JavaScript, and modern frameworks like React for front-end
        development. Skilled in server-side languages such as Node.js and
        Python, with experience in database management using SQL and MongoDB.
        Capable of creating responsive and user-friendly web applications from
        concept to deployment. Strong problem-solving abilities and a proactive
        approach to learning new technologies and methodologies. Collaborative
        team player with excellent communication skills, eager to contribute to
        innovative projects and grow professionally in a dynamic environment.
      </p>
      <br />
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
        &nbsp;&nbsp;&nbsp;&nbsp; I have a strong passion for technology and
        computers. I initially attended Pennsylvania College of Technology to
        pursue a degree in Electronics and Computer Engineering Technology with
        an emphasis on Robotics and Automation. One of the classes that stood
        out to me was Introduction to Microprocessors, where I learned how to
        code Zybo boards using the C programming language and make the LEDs
        light up in different sequences depending on the analog input. When I
        graduated, I realized that what I had studied was not what I wanted to
        pursue as a career. I decided to follow a different path and became very
        interested in coding, specifically web development. Outside of
        programming, I have a hobby of learning about and engaging with
        technology. I enjoy tinkering with my Arch Linux operating system, which
        I use as my daily driver, and building PCs for people while teaching
        them about Linux.
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
