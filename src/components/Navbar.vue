<template>
   <header>
      <div class="menu">
         <div class="line-1"></div>
         <div class="line-2"></div>
      </div>
      <h3>Joker</h3>
      <button>TICKETS</button>
   </header>
</template>

<script>
   export default {
      name: "Navbar",
   };
</script>

<style lang="scss" scoped>
   header {
      width: 100%;
      height: 40px;
      position: absolute;
      top: 60px;
      display: flex;
      align-items: center;

      .menu {
         width: 50px;
         height: 20px;
         display: flex;
         flex-direction: column;
         justify-content: space-between;
         position: absolute;
         left: 80px;
         z-index: 2;
         cursor: pointer;

         .line-1 {
            width: 50px;
            height: 4px;
            background-color: #fff;
         }

         .line-2 {
            width: 30px;
            height: 4px;
            background-color: #fff;
         }
      }

      h3 {
         width: fit-content;
         font-family: Inter;
         font-size: 2.8rem;
         color: #fff;
         user-select: none;
         position: absolute;
         left: 0;
         right: 0;
         margin: auto;
      }

      button {
         width: 140px;
         height: 40px;
         border: 2px solid #e52e3e;
         outline: none;
         font-family: Inter, Malgun;
         font-size: 1.4rem;
         color: #fff;
         cursor: pointer;
         z-index: 5;
         position: absolute;
         background-color: transparent;
         right: 80px;
      }
   }
   @media (max-width: 886px) {
      header {
         top: 20px;

         .menu {
            left: 20px;
         }
         h3 {
            font-size: 2rem;
         }
         button {
            width: 120px;
            border-radius: 20px;
            font-size: 1.2rem;
            right: 20px;
         }
      }
   }
</style>
