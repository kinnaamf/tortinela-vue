<template>
  <nav>
    <ul class="list">
      <li><a href="" class="nav-link">Acasă</a></li>
      <li><a href="" class="nav-link">Promoții</a></li>
      <li><a href="" class="nav-link">Recenzii</a></li>
    </ul>
  </nav>
</template>

<style scoped lang="postcss">
.nav-link {
  @apply 2xl:hover:underline 2xl:transition-all 2xl:duration-200 2xl:hover:text-[#BC7E2D];
}

.list {
  @apply 2xl:flex 2xl:uppercase 2xl:gap-16 2xl:text-xl 2xl:font-medium;
}
</style>