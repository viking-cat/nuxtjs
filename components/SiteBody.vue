<template>
  <div id="siteBody">
    <Nuxt/>
  </div>
</template>

<style>
  #siteBody {
    flex-grow: 2;
    width: 100%;
    padding: 16px 16px 16px 16px;
    /*background-color: #2e294e;*/
    background-image: radial-gradient(
        /*#ffd400 2px,*/
        #444488 1px,
        transparent 1px
    );
    background-size: 8px 8px;
  }
</style>
