<template>
  <div>
    <VideoBackground :src="require(`@/assets/comingsoon.mp4`)" style="height: 100vh;" />
    <div class="container">
      <img alt="Simmaster logo" :src="require(`@/assets/logo.png`)">
      <h1>SPREMITE SE ZA TRKU 🏁</h1>
    </div>
  </div>
</template>

<script>
 import VideoBackground from 'vue-responsive-video-background-player'

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components: { VideoBackground },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  display: flex;
  align-items: center;
  width: 100%;
  position: absolute;
  opacity: 0.8;
  top: 0;
  left: 0;
}

span {
  font-size: 2rem;
  color: white;
  font-family: Formula1, sans-serif !important;
}

h1 {
  font-family: Formula1, sans-serif !important;
  width: fit-content;
  color: white;
  overflow: hidden; /* Ensures the content is not revealed until the animation */
  white-space: nowrap; /* Keeps the content on a single line */
  margin: 0 auto; /* Gives that scrolling effect as the typing happens */
  letter-spacing: .15em; /* Adjust as needed */
  align-self: flex-start;
  transform: translateY(50px);
}

@media screen and (max-width: 768px) {
  img {
    max-height: 100px;
  }

  h1 {
    font-size: 1.5rem;
  }

  .container {
    display: flex;
    flex-direction: column;
  }
}

img {
  max-height: 300px
}


</style>
