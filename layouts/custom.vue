<template>
  <div class="container">
    <header class="top-header">
      <div></div>
      <NuxtLink to="/"><span>Home</span></NuxtLink>
      <NuxtLink to="/about"><span>About</span></NuxtLink>
      <NuxtLink to="/more"><span>More content</span></NuxtLink>
      <div></div>
    </header>
    <main>
      <slot />
    </main>
  </div>
</template>
<style lang="scss">
$border-weak: 2px solid #bbb;
$border-stronk: 2px solid #000;


body {
  margin: 0px;
  background-color: #ddd;
}


* {
  box-sizing: border-box;
}

main {
  >* {
    display: flex;
    flex-flow: column nowrap;
  }

  hr {
    width: 100%;
  }

  p {
    margin-bottom: 0;
  }

  grid-column: 2/3;
  padding: 18px;
  background-color: #eee;
  box-shadow: 0px 0px 2px 2px #ccc inset;

  * {
    clear: both;

  }


  .link {
    background-color: #000;
    margin: 8px;
    text-align: center;
    display: grid;
    place-content: center;
    padding: 12px;
    text-decoration: none;
    color: white;

    &:hover {
      background: #333;
    }
  }

  @media (max-width: 1024px) {
    grid-column: 1/-1;
    margin: 12px;
  }

}

.container {
  display: grid;
  grid-template-rows: 70px auto;
  grid-template-columns: 20% auto 20%;

  @media (max-width: 1024px) {
    grid-template-columns: 1fr;
  }
}

.top-header {
  display: flex;
  justify-items: start;
  margin: 12px;
  grid-column: 1/-1;
  >div:last-child{
    width: 100%;
    border-bottom: $border-weak;
    
  }
  >a {
    border-bottom: $border-weak;
    padding: 8px 16px;
    text-decoration: none;
    color: black;
    display: grid;
    place-content: center;
    text-align: center;

    &:hover {
      border-bottom: $border-stronk;
    }

    &.router-link-active {
      border-bottom: none;
      border-top: $border-weak;
      border-left: $border-weak;
      border-right: $border-weak;
      // the active link
    }
  }
}</style>