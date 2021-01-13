<template>
   <section>
      <div id="frame"></div>
      <div id="background" alt="joker_cover" />
   </section>
</template>

<script>
   export default {
      name: "Background",
   };
</script>

<style lang="scss" scoped>
   #frame {
      width: 100%;
      height: 100vh;
      border: 15px solid black;
      background-color: transparent;
      position: absolute;
      z-index: 2;
   }
   #background {
      background-image: url("./../assets/joker-background.jpg");
      width: 100%;
      height: 100vh;
      background-size: cover;
      background-position: 80% 40%;
   }
   @media (max-width: 886px) {
      #frame {
         display: none;
      }
   }
</style>
