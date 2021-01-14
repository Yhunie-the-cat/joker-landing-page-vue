<template>
   <div id="social-container">
      <a
         href="https://www.facebook.com/jokermovie/"
         target="_blank"
         rel="noopener noreferrer"
      >
         <img src="./../assets/facebook.png" alt="facebook" />
      </a>
      <a
         href="https://www.instagram.com/jokermovie/"
         target="_blank"
         rel="noopener noreferrer"
      >
         <img src="./../assets/instagram.png" alt="instagram" />
      </a>
      <a
         href="https://twitter.com/jokermovie"
         target="_blank"
         rel="noopener noreferrer"
      >
         <img src="./../assets/twitter.png" alt="twitter" />
      </a>
   </div>
</template>

<script>
   export default {
      name: "Socialbar",
   };
</script>

<style lang="scss" scoped>
   #social-container {
      position: absolute;
      height: 180px;
      top: 0;
      bottom: 0;
      right: 40px;
      margin: auto;
      z-index: 5;
      display: flex;
      flex-direction: column;
      img {
         width: 15px;
         height: 15px;
         margin: 20px 0;
         cursor: pointer;
      }
   }
   @media screen and (max-width: 425px) {
      #social-container {
         right: 20px;
      }
   }
</style>
