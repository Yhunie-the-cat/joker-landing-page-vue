<template>
   <section>
      <h1 id="big-title">JOKER</h1>
      <h2 id="small-title">JOKER</h2>
      <h4 id="quote">"PUT ON A HAPPY FACE"</h4>
      <p id="main">Joaquin Phoenix</p>
      <p id="support">Robert De Niro</p>

      <div id="cinema-date">
         <h4 style="color: #5e5e5e;">IN CINEMAS</h4>
         <h4>OCTOBER 4</h4>
      </div>
   </section>
</template>

<script>
   export default {
      name: "TextContent",
   };
</script>

<style lang="scss" scoped>
   @mixin text {
      width: fit-content;
      font-family: Nanum Gothic, sans-serif;
      font-size: 1.4rem;
      font-weight: 600;
      color: #fff;
      position: absolute;
      z-index: 2;
   }

   #big-title {
      width: 100%;
      height: fit-content;
      position: absolute;
      top: 0;
      bottom: 0;
      transform: translateX(-8%);
      margin: auto;
      z-index: 1;
      font-family: Monda, sans-serif;
      font-size: 40rem;
      color: transparent;
      -webkit-text-stroke-width: 1px;
      -webkit-text-stroke-color: #bcbcbc;
      animation: appeartext 3s ease-in-out;
      @keyframes appeartext {
         from {
            opacity: 0;
         }
         to {
            opacity: 1;
         }
      }
   }

   #small-title {
      width: fit-content;
      height: fit-content;
      position: absolute;
      top: 0;
      bottom: 0;
      left: 18%;
      z-index: 2;
      margin: auto;
      font-family: Monda, sans-serif;
      font-size: 8rem;
      color: #fff;
      animation: slidefrombottom 3s ease-in-out;
      @keyframes slidefrombottom {
         0% {
            transform: translateY(100%);
            opacity: 0;
         }
         20% {
            opacity: 0;
         }

         100% {
            transform: translateY(0);
            opacity: 1;
         }
      }
   }

   #quote {
      width: fit-content;
      font-family: Monda, sans-serif;
      font-size: 2rem;
      letter-spacing: 0.1rem;
      color: #e52e3e;
      text-shadow: 4px 4px 8px black;
      position: absolute;
      z-index: 2;
      bottom: 300px;
      left: 30%;
      animation: slidefromright 3s ease-in-out;
      @keyframes slidefromright {
         from {
            transform: translateX(-200%);
            opacity: 0;
         }
         to {
            transform: translateX(0);
            opacity: 1;
         }
      }
   }

   #main {
      @include text();
      top: 260px;
      left: 16%;
      animation: slidefromright 2s ease-in-out;
      @keyframes slidefromright {
         from {
            transform: translateX(-100%);
            opacity: 0;
         }
         to {
            transform: translateX(0);
            opacity: 1;
         }
      }
   }

   #support {
      @include text();
      top: 300px;
      left: 28%;
      animation: slidefromleft 2s ease-in-out;
      @keyframes slidefromleft {
         from {
            transform: translateX(100%);
            opacity: 0;
         }
         to {
            transform: translateX(0);
            opacity: 1;
         }
      }
   }

   #cinema-date {
      position: absolute;
      z-index: 2;
      bottom: 230px;
      left: 37%;
      display: flex;
      h4 {
         width: fit-content;
         font-family: Nanum Gothic, sans-serif;
         font-size: 1.4rem;
         color: #fff;
         margin: 0 10px;
      }
   }
   #cinema-date:first-child {
      color: #5e5e5e;
   }

   @media (max-width: 886px) {
      #big-title {
         display: none;
      }
      #small-title {
         display: none;
      }
      #quote {
         bottom: 80px;
         left: 12%;
      }

      #cinema-date {
         bottom: 160px;
      }
      #main {
         top: 160px;
         left: 12%;
         font-size: 1.2rem;
      }
      #support {
         top: 240px;
         left: 20%;
         font-size: 1.2rem;
      }
   }
   @media (max-width: 560px) {
      #quote {
         left: 0;
         right: 0;
         margin: auto;
         font-size: 1.6rem;
      }
      #cinema-date h4 {
         font-size: 1.2rem;
      }
   }
</style>
