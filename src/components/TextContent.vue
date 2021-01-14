<template>
   <section>
      <h1 id="big-title">JOKER</h1>

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
      margin: auto;
      z-index: 1;
      font-family: Monda, sans-serif;
      font-size: 30vmax;
      color: transparent;
      overflow: hidden;
      -webkit-text-stroke-width: 1px;
      -webkit-text-stroke-color: #bcbcbc;
      animation: slidefrombottom 3s ease-in-out;
      @keyframes slidefrombottom {
         0% {
            transform: translateY(20%);
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
      font-family: Inter, sans-serif;
      font-size: 1.6rem;
      letter-spacing: 0.1rem;
      color: #e52e3e;
      text-shadow: 4px 4px 8px black;
      position: absolute;
      z-index: 2;
      bottom: 260px;
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
      top: 340px;
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
      bottom: 40px;
      right: 40px;
      display: flex;
      h4 {
         width: fit-content;
         font-family: Nanum Gothic, sans-serif;
         font-size: 1.2rem;
         color: #fff;
         margin: 0 10px;
      }
   }
   #cinema-date:first-child {
      color: #5e5e5e;
   }
   @media screen and (max-width: 1024px) {
      #big-title {
         font-size: 25vmax;
      }
   }
   @media screen and (max-width: 768px) {
      #big-title {
         font-size: 25vmin;
      }
      #quote {
         left: 0;
         right: 0;
         margin: auto;
      }
   }
   @media screen and (max-width: 425px) {
      #big-title {
         font-size: 10vmax;
      }
      #support {
         top: 300px;
      }
      #quote {
         bottom: 200px;
      }
   }
</style>
