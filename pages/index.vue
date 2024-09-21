<template>
  <div class="container mx-auto py-5">
    <h1 class="text-2xl text-slate-700 font-bold">
      Bienvenido al portal Fiduciario
    </h1>
    <h2 class="text-sm">
      Consulte y administre sus fideicomisos.
    </h2>
    <div class="flex">
      <div class="w-3/5 p-3">
        <UiCard class="mb-3">
          <h2 class="text-xl text-slate-700 font-bold">
            Saldos
          </h2>
          <p>Saldos por fideicomisos</p>
          <UiTable :headers="[
            { label: 'Fideicomiso', name: 'name'},
            { label: 'Saldo total', name: 'balance'},
            { label: 'Saldo disponible', name: 'available'},
            { label: 'Fecha', name: 'date'}
          ]" :data="[
            { name: 'Fideicomiso 1', balance: '$1,000,000.00', available: '$500,000.00', date: '2021-10-01'},
            { name: 'Fideicomiso 2', balance: '$2,000,000.00', available: '$1,000,000.00', date: '2021-10-01'},
            { name: 'Fideicomiso 3', balance: '$3,000,000.00', available: '$1,500,000.00', date: '2021-10-01'}
          ]">
          </UiTable>
        </UiCard>
        <UiCard class="mb-3">
          <h2 class="text-xl text-slate-700 font-bold">
            Movimientos
          </h2>
          <p>Movimientos por fics</p>
          <UiTable :headers="[
            { label: 'Fecha', name: 'date', classes: 'w-32'},
            { label: 'Fic', name: 'name'},
            { label: 'Descripcion', name: 'description'},
            { label: 'Movimiento', name: 'movement'},
            { label: 'Valor', name: 'ammount'}
          ]" :data="[
            {
              name: 'Fic Prueba | 93910000012',
              description: 'Compra de terreno para parqueadero de prueba direccion 1',
              ammount: '$500,000.00',
              date: '2021-10-01',
              movement: 'Debito'
            },
            {
              name: 'Fic Prueba | 93910000012',
              description: 'Compra de terreno para parqueadero de prueba direccion 2',
              ammount: '$500,000.00',
              date: '2021-10-01',
              movement: 'Debito'
            },
            {
              name: 'Fic Prueba | 93910000012',
              description: 'Compra de terreno para parqueadero de prueba direccion 3',
              ammount: '$500,000.00',
              date: '2021-10-01',
              movement: 'Debito'
            }
          ]">
          </UiTable>
        </UiCard>
      </div>
      <div class="w-2/5 p-3">
        <UiCard>
          <h2 class="text-xl text-slate-700 font-bold">
            Información contable y financiera
          </h2>
          <p class="mb-3">
            Descargue aquí los documentos que contienen la información financiera de sus fideicomisos los cuales son: (Estado financiero con terceros, Estado financiero sin terceros, Balances de prueba).
          </p>
          <div class="mb-3">
            <label for="Tipo">Tipo de documento</label>
            <select id="Tipo" class="w-full p-3 border border-gray-300 rounded-lg">
              <option value="1">Estado financiero con terceros</option>
              <option value="2">Estado financiero sin terceros</option>
              <option value="3">Balances de prueba</option>
              <option value="4">Extractos</option>
            </select>
          </div>
          <div class="mb-3">
            <label for="account">Fideicomiso</label>
            <select id="account" class="w-full p-3 border border-gray-300 rounded-lg">
              <option value="1">Fideicomiso 1</option>
              <option value="2">Fideicomiso 2</option>
              <option value="3">Fideicomiso 3</option>
            </select>
          </div>
          <button class="bg-red-500 text-white px-4 py-2 rounded">
            <i class="mdi mdi-magnify"></i>
            Consultar
          </button>
        </UiCard>
      </div>
    </div>
  </div>
</template>