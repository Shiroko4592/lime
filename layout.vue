<template>
  <div class="darknet-layout">
    <div class="warning-banner">Warning: You are accessing a darknet resource!</div>
    <div class="terminal">
      <p class="encrypted-text">Loading...</p>
      <p class="glitch-effect">Welcome to the dark web!</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Layout',
};
</script>

<style scoped>
.darknet-layout {
  background-color: #000;
  color: #0f0;
  border: 5px solid #ff00ff;
  font-family: 'Courier New', Courier, monospace;
  overflow: hidden;
}

.warning-banner {
  background-color: red;
  color: white;
  padding: 10px;
  text-align: center;
  animation: fade-in 3s;
}

.encrypted-text {
  font-weight: bold;
  letter-spacing: 2px;
  filter: blur(1px);
  animation: scramble 5s infinite;
}

.glitch-effect {
  color: #ff00ff;
  animation: glitch 1s infinite;
}

@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes scramble {
  0%, 100% { filter: blur(1px); }
  50% { filter: blur(5px); }
}

@keyframes glitch {
  0% { text-shadow: 1px 1px #ff0000; }
  25% { text-shadow: -1px -1px #00ff00; }
  50% { text-shadow: 1px -1px #0000ff; }
  75% { text-shadow: -1px 1px #ffff00; }
  100% { text-shadow: none; }
}
</style>
