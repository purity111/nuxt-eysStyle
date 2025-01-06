<template>
  <div
    class="mt-[15px] lg:mt-[40px] relative bg-[url('/img/sp/bg-imgs.avif')] lg:bg-[url('/img/pc/bg-imgs.avif')] about-bg"
  >
    <div class="relative z-20">
      <MoleculesEnjoyContents />
      <MoleculesBanner class="pt-[75px] lg:pt-[200px]" />
    </div>
  </div>
</template>

<style scoped>
@media (min-width: 376px) {
  .about-bg {
    background-size: cover;
    background-position: center;
  }
}
@media (min-width: 1900px) {
  .about-bg {
    background-size: unset;
    background-position: unset;
  }
}
@media (min-width: 1921px) {
  .about-bg {
    background-size: cover;
    background-position: center;
  }
}
</style>
