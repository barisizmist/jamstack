<template>
  <img class="jamstack-logo" alt="Jamstack Logo" src="/jamstack-logo.png" />
</template>

<style>
.jamstack-logo {
  height: 140px;
  width: 140px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
  margin-left: 20px !important;
}
@media screen and (max-width: 920px) {
  .jamstack-logo {
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
