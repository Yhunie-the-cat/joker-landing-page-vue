<template>
   <header>
      <div class="menu">
         <div class="line-1"></div>
         <div class="line-2"></div>
      </div>
      <h3>Joker</h3>
      <a
         href="https://www.hulu.com/movie/joker-49d3d249-a81b-4606-a37c-c7249f9b2ce0"
         target="_blank"
         rel="noopener noreferrer"
      >
         <button>WATCH</button>
      </a>
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
      top: 40px;
      display: flex;
      align-items: center;

      .menu {
         width: 50px;
         height: 20px;
         display: flex;
         flex-direction: column;
         justify-content: space-between;
         position: absolute;
         left: 40px;
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
         font-family: Monda;
         font-size: 1.6rem;
         font-size: 1.6rem;
         color: #fff;
         user-select: none;
         position: absolute;
         left: 0;
         right: 0;
         margin: auto;
      }

      button {
         width: 120px;
         height: 40px;
         border: 2px solid #e52e3e;
         outline: none;
         font-family: Inter, Malgun;
         font-size: 1rem;
         color: #fff;
         cursor: pointer;
         z-index: 5;
         position: absolute;
         background-color: transparent;
         right: 40px;
      }
   }

   @media screen and (max-width: 425px) {
      header {
         .menu {
            left: 20px;
         }

         button {
            width: 80px;
            border-radius: 40px;
            right: 20px;
         }
      }
   }
</style>
