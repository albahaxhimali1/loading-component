<template>
  <div class="loading-container">

  </div>
</template>
<style lang="scss" scoped>
  .loading-container {
    width: 250px;
    height: 250px;
    border-radius: 50%;
    box-sizing: border-box;
    border-top: 10px solid #f1c40f;
    position: relative;
    animation: load 2s linear infinite;

    &:before, &:after {
      content: '';
      width: 250px;
      height: 250px;
      position: absolute;
      left: 0;
      top: -12px;
      border-radius: 50%;
      box-sizing: border-box;
    }

    &:before {
      border-top: 10px solid #e74c3c;
      transform: rotate(120deg);
    }

    &:after {
      border-top: 10px solid #1abc9c;
      transform: rotate(240deg);
    }
    
    @keyframes load {
      to {
        transform: rotate(360deg);
      }
    }
  }

</style>
