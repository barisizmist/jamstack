<template>
  <img class="VuetifyLogo" alt="Vuetify Logo" src="/vuetify-logo.svg" />
</template>

<style>
.VuetifyLogo {
  height: 140px;
  width: 140px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}
@media screen and (max-width: 920px) {
  .VuetifyLogo {
    height: 60px;
    width: 60px;
  }
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>
