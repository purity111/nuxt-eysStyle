<template>
  <div class="flex items-center justify-between">
    <span class="hidden lg:block opacity-0 w-[1px] h-[1px]"></span>
    <AtomsToTopBtn
      :icon="'/img/common/msg.svg'"
      class="h-[40px] w-[305px] lg:w-[340px] lg:h-[50px] shadow"
      :text="'お得なメールマガジンに登録'"
    />
    <img
      class="w-[40px] lg:w-[50px] shadow"
      src="/img/common/totop.png"
      alt="アートタイトル"
      loading="lazy"
      decoding="async"
    />
  </div>
</template>

<style scoped>
.shadow {
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
}
</style>
