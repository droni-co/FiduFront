<template>
  <div class="container mx-auto py-5">
    <h1 class="text-2xl text-slate-700 font-bold">
      Saldos y movimientos
    </h1>
    <h2 class="text-sm">
      Consulte saldos y movimientos por fideicomisos y fics
    </h2>

    <div class="grid grid-cols-3 gap-4 mt-5">
      <NuxtLink to="/saldos/100284">
        <TrustCard class="transition hover:bg-slate-100 hover:shadow-xl" />
      </NuxtLink>
      <NuxtLink to="/saldos/100284">
        <TrustCard class="transition hover:bg-slate-100 hover:shadow-xl" />
      </NuxtLink>
    </div>
  </div>
</template>