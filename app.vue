<template>
  <div class="gallery">
    <div class="card latched">
      <section
        class="card latched flex flex-col justify-start content-start bg-black p-20 text-zinc-50"
      >
        <div class="headlineDiv h-2/3">
          <span class="headline font-semibold">I'm Niall</span>
          <span class="headline font-semibold">Portfolio/24</span>
        </div>
        <nav>
          <ul class="menu">
            <li>Projects</li>
            <li>Contacts</li>
          </ul>
        </nav>
        <div>
          <div class="frontEndDeveloperDiv">
            <div class="frontEndDeveloper">Frontend Developer</div>
            <div class="frontEndDeveloper">
              ✺Here you can see some of my latest designs and projects
            </div>
          </div>
        </div>
      </section>
    </div>
    <div class="spacer"></div>

    <!-- INTRODUCTION TO ME -->
    <div class="card">
      <section class="card bg-white p-11 h-lvh flex flex-col">
        <div class="container mx-auto px-80">
          <div class="">
            <h1 class="aboutMeText text-black text-center">
              Crafting nice and useful things for people
            </h1>
          </div>
          <p class="text-center text-black px-24 py-5">
            I AM CURRENTLY PART OF THE DESIGN TEAM AT EGGS DESIGN﻿ IN MADRID,
            AND I HAVE HAD THE OPPORTUNITY TO HELP CREATE DIGITAL EXPERIENCES
            AND SOLUTIONS FOR BIG BRANDS FOR THE LAST 20 YEARS OF MY LIFE. I
            CONSIDER MYSELF PASSIONATE ABOUT TECHNOLOGY, WORKING AT THE
            INTERSECTION BETWEEN BRANDING AND DIGITAL PRODUCT DESIGN.
          </p>
          <p class="text-center text-black px-24 py-5">
            NOW, I WORK HAND IN HAND WITH BBVA DESIGN AND USER EXPERIENCE TEAM
            HELPING TO IMPROVE THEIR DIGITAL PRODUCTS BY BALANCING BUSINESS
            PRIORITIES WITH THOSE OF THE THOUSANDS OF USERS WHO USE THEIR
            SERVICES. FROM THE EARLY STAGES OF DEFINITION AND IDEATION, TO THE
            REVIEW OF INTERACTION FLOWS AND USER TESTING.
          </p>
          <p class="text-center text-black px-24 py-5">
            PREVIOUSLY I HAD THE OPPORTUNITY TO COLLABORATE WITH REPSOL'S DESIGN
            TEAM, FROM UX TO VISUAL PROCESSES, HELPING LAUNCH FUNCTIONALITIES
            FOCUSED WHERE REPSOL CURRENTLY OPERATES.
          </p>
          <img src="" alt="" />
        </div>
      </section>
    </div>
    <div class="spacer"></div>

    <!-- WHAT I DO -->
    <div class="card">
      <section class="card skillsDiv bg-slate-400 p-11 h-lvh">
        <div class="skills flex flex-col">
          <span class="whatIDo">Product design</span>
          <span class="whatIDo">User experience</span>
          <span class="whatIDo">UI design</span>
          <span class="whatIDo">Visual design</span>
        </div>
      </section>
    </div>
    <div class="spacer"></div>

    <!-- RECENT WORK1 -->
    <div class="card bg-black w-full text-center justify-center">
      <!-- <section> -->
      <h1
        class="recentWork flex justify-center content-center flex-wrap bg-black text-zinc-50"
      >
        Recent work
      </h1>
      <!-- </section> -->
    </div>
    <div class="spacer"></div>

    <!-- RECENT WORK2 -->
    <div class="card">
      <section class="card bg-slate-300 p-11 h-lvh">
        <div
          class="content-center justify-center flex flex-wrap bg-slate-400 py-5"
        >
          <div class="mx-auto flex justify-center flex flex-wrap">
            <img
              class="projectImg"
              src="https://placehold.co/1600x1000"
              alt=""
            />
          </div>
          <div class="container">
            <div class="project">Roazhon Goal Academy</div>
            <div class="project-description"></div>
            <div>PRODUCT DESIGN / VISUAL DESIGN / CONCEPT</div>
          </div>
        </div>
      </section>
    </div>
    <div class="spacer"></div>
    <!-- FOOTER -->
    <div class="card">
      <footer class="card bg-slate-200 p-11 h-96 flex justify-between">
        <h1 class="footerTitle">Tell me something cool or just troll me.</h1>
        <div id="contactMe">
          <ul>
            <li>instagram</li>
            <li>Linktree</li>
            <li>email</li>
          </ul>
        </div>
      </footer>
    </div>
    <div class="spacer"></div>
  </div>
</template>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  var positions = [];
  var cards = document.querySelectorAll(".card");

  cards.forEach(function (card) {
    positions.push(card.getBoundingClientRect().top + window.scrollY);
  });

  window.addEventListener("scroll", function () {
    var pos = window.scrollY || window.pageYOffset;

    for (var i = 0; i < cards.length; i++) {
      if (pos >= positions[i]) {
        cards[i].classList.add("latched");
      } else {
        cards[i].classList.remove("latched");
      }
    }
  });
});
</script>

<style scoped></style>
