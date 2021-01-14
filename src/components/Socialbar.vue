<template>
   <div id="social-container">
      <img src="./../assets/facebook.png" alt="facebook" />
      <img src="./../assets/instagram.png" alt="instagram" />
      <img src="./../assets/twitter.png" alt="twitter" />
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
