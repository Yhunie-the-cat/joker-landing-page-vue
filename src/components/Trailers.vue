<template>
   <section id="trailers-container">
      <div>
         <p>Final trailer</p>
         <video
            src="https://www.youtube.com/watch?v=zAGVQLHvwOY"
            type="video/mp4"
            poster="./../assets/joker-final-thumbnail.jpg"
            preload="metadata"
            controlsList="nodownload"
            muted
            loop
         ></video>
      </div>

      <div>
         <p>Final trailer</p>
         <video
            src="https://www.youtube.com/watch?v=zAGVQLHvwOY"
            type="video/mp4"
            poster="./../assets/joker-teaser-thumbnail.jpg"
            preload="metadata"
            controlsList="nodownload"
            muted
            loop
         ></video>
      </div>
   </section>
</template>

<script>
   export default {
      name: "Trailers",
   };
</script>

<style lang="scss" scoped>
   #trailers-container {
      z-index: 6;
      position: absolute;
      width: 640px;
      height: 140px;
      bottom: 60px;
      left: 15%;
      display: flex;
      justify-content: space-between;

      div {
         width: 300px;

         p {
            font-family: Nanum Gothic, Malgun;
            font-size: 1rem;
            font-weight: 600;
            color: #5e5e5e;
            float: right;
            margin-bottom: 5px;
         }

         video {
            width: 300px;
            height: 80px;
            object-fit: cover;
            pointer-events: visible;
            cursor: pointer;
         }
      }
   }
   @media (max-width: 886px) {
      #trailers-container {
         flex-direction: column;
         width: fit-content;
         height: fit-content;
         bottom: 200px;

         div {
            margin: 20px 0;
            p {
               color: white;
            }
         }
      }
   }
</style>
