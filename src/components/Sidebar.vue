<template>
   <div id="page-lines-container">
      <div class="line active"></div>
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
   </div>
</template>

<script>
   export default {
      name: "Sidebar",
   };
</script>

<style lang="scss" scope>
   #page-lines-container {
      width: fit-content;
      height: 58px;
      position: absolute;
      left: 80px;
      top: 0;
      bottom: 0;
      margin: auto;
      .line {
         width: 10px;
         height: 2px;
         margin: 10px 0;
         background-color: #fff;
      }
      .active {
         background-color: #e52e3e !important;
      }
   }
   @media (max-width: 886px) {
      #page-lines-container {
         left: 20px;
      }
   }
</style>
