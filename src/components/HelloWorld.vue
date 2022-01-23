<template>
  <div>
    <div class="typewriter">
      <h1>Get ready to race 🏁</h1>
    </div>
    <VideoBackground :src="require(`@/assets/comingsoon.mp4`)" style="height: 100vh;" />
    <div class="container">
      <img alt="Simmaster logo" :src="require(`@/assets/logo.png`)" style="max-height: 250px;">
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
  opacity: 0.4;
  top: 0;
  left: 0;
}

span {
  font-size: 2rem;
  color: white;
  font-family: "Bull", sans-serif !important;
}

.typewriter h1 {
  width: fit-content;
  color: white;
  overflow: hidden; /* Ensures the content is not revealed until the animation */
  border-right: .15em solid orange; /* The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  margin: 0 auto; /* Gives that scrolling effect as the typing happens */
  letter-spacing: .15em; /* Adjust as needed */
  animation: 
    typing 3.5s steps(40, end),
    blink-caret 1.5s step-end infinite;
}

/* The typing effect */
@keyframes typing {
  from { width: 0 }
  to { width: 25% }
}

/* The typewriter cursor effect */
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: red; }
}

</style>
