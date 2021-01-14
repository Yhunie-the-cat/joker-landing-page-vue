<template>
   <div id="app">
      <Navbar />
      <TextContent />
      <Sidebar />
      <Socialbar />
      <Trailers />
      <Background />
   </div>
</template>

<script>
   import Navbar from "./components/Navbar.vue";
   import TextContent from "./components/TextContent.vue";
   import Sidebar from "./components/Sidebar";
   import Socialbar from "./components/Socialbar";
   import Trailers from "./components/Trailers";
   import Background from "./components/Background.vue";

   export default {
      name: "App",
      components: {
         Navbar,
         TextContent,
         Sidebar,
         Socialbar,
         Trailers,
         Background,
      },
   };
</script>

<style>
   * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
   }

   html {
      font-size: 16px;
      width: 100%;
      height: 100vh;
   }

   @media screen and (max-width: 1024px) {
      html {
         font-size: 15px;
      }
   }

   @media screen and (max-width: 768px) {
      html {
         font-size: 12px;
      }
   }

   @media screen and (max-width: 425px) {
      html {
         font-size: 10px;
      }
   }

   @import url("https://fonts.googleapis.com/css2?family=Nanum+Gothic:wght@400;700&display=swap");
   @import url("https://fonts.googleapis.com/css2?family=Monda:wght@400;700&display=swap");
   @import url("https://fonts.googleapis.com/css2?family=Inter&display=swap");

   #app {
      font-family: Nanum Gothic, Inter, Monda, Avenir, Helvetica, Arial,
         sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
   }
</style>
