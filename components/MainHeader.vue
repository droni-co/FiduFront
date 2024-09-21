<template>
  <header class="bg-slate-700">
    <div class="container mx-auto py-4 flex">
      <img src="~/assets/img/logo.png" class="rounded bg-white p-2 h-16" alt="Fiduciaria" />
      <div class="p-2 text-slate-100 text-sm grow text-end">
        <p>
          Bienvenido(a) <strong>Kalvin Manson2</strong><br>
          Última conexión: 2021-09-01 12:00:00
        </p>
        <a href="#" class="text-slate-100 hover:text-slate-200">
          <i class="mdi mdi-logout"></i>
          Cerrar sesión
        </a>
      </div>
    </div>
    <nav class="bg-slate-100 shadow">
      <div class="container mx-auto flex">
        <NuxtLink to="/" class="p-3 text-red-600 border-r border-slate-300 transition hover:text-red-800">
          <i class="mdi mdi-home text-lg"></i>
        </NuxtLink>
        <NuxtLink to="/contable" class="p-4 text-slate-600 hover:text-slate-800 font-bold">
          Información contable y financiera
        </NuxtLink>
        <NuxtLink to="/saldos" class="p-4 text-slate-600 hover:text-slate-800 font-bold">
          Saldos y movimientos
        </NuxtLink>
        <a href="#" class="p-4 text-slate-600 hover:text-slate-800 font-bold">
          Transacciones
        </a>
      </div>
    </nav>
  </header>
</template>