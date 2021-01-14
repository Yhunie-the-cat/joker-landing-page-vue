<template>
   <div id="covers">
      <div>
         <p>Final trailer</p>
         <a href="https://www.youtube.com/watch?v=zAGVQLHvwOY" target="_blank">
            <img
               src="./../assets/joker-final-thumbnail.jpg"
               alt="final-trailer-cover"
            />
         </a>
      </div>

      <div>
         <p>Teaser trailer</p>
         <a href="https://www.youtube.com/watch?v=t433PEQGErc" target="_blank">
            <img
               src="./../assets/joker-teaser-thumbnail.jpg"
               alt="teaser-trailer-cover"
            />
         </a>
      </div>
   </div>
</template>

<script>
   export default {
      name: "Trailers",
   };
</script>

<style lang="scss" scoped>
   #covers {
      width: fit-content;
      display: flex;
      position: absolute;
      bottom: 40px;
      left: 40px;
      z-index: 10;
      div {
         width: 300px;

         p {
            font-family: Inter, Malgun;
            font-size: 1rem;
            font-weight: 400;
            color: white;
            float: right;
            margin-bottom: 5px;
         }
         img {
            width: 100%;
            height: 80px;
            object-fit: cover;
            pointer-events: visible;
            cursor: pointer;
         }
      }
      div:first-child {
         margin-right: 40px;
      }
   }

   @media screen and (max-width: 1024px) {
      #covers div {
         width: 200px;
         img {
            height: 60px;
         }
      }
   }

   @media screen and (max-width: 768px) {
      #covers {
         bottom: 100px;
         left: 0;
         right: 0;
         margin: auto;
         div {
            width: 160px;
         }
         div:first-child {
            margin-right: 20px;
         }
      }
   }
   @media screen and (max-width: 425px) {
      #covers div {
         width: 40vmin;
      }
   }
</style>
