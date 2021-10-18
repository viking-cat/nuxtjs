<template>
  <div id="page">
    <SiteHeader />
    <SiteBody />
    <SiteFooter />
  </div>
</template>

<style>
* {
  box-sizing: border-box;
}

html, body, #__nuxt, #__layout {
  height:100%;
  margin: 0px;
  background-color: #000000;
  color: #ffffff;
}

#page {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  align-content: stretch;
  /*justify-content: center;*/
  margin: auto;
  width: 1024px;
  height: 100%;
}
</style>
