<template>
  <div class="container mx-auto py-5">
    <h1 class="text-2xl text-slate-700 font-bold">
      Información contable y financiera
    </h1>
    <h2 class="text-sm">
      Descargue aquí los documentos que contienen la información financiera de sus fideicomisos los cuales son: (Estado financiero con terceros, Estado financiero sin terceros, Balances de prueba).
    </h2>
    <!-- Filters -->
    <UiCard class="flex my-5">
      <div>
        <label for="client" class="mr-2 text-sm">Cliente:</label>
        <UiFormSelect id="client" value="1" :options="[
          { id: 0, name: 'Todos' },
          { id: 1, name: 'Droni.co' }
        ]" />
      </div>
      <div class="ms-2">
        <label for="trust" class="mr-2">Fideicomiso:</label>
        <UiFormSelect id="trust" :options="[
          { id: 0, name: 'Todos' },
          { id: 'Fideicomiso prueba', name: 'Fideicomiso prueba' },
          { id: 'Fideicomiso prueba 2', name: 'Fideicomiso prueba 2' }
        ]" />
      </div>
      <div class="ms-2">
        <label for="fic" class="mr-2">FIC:</label>
        <UiFormSelect id="fic" :options="[
          { id: 0, name: 'Todos' },
          { id: 'FIC-001', name: 'FIC-001' },
          { id: 'FIC-002', name: 'FIC-002' },
          { id: 'FIC-003', name: 'FIC-003' }
        ]" />
      </div>
      <div class="ms-2">
        <label for="year" class="mr-2">Año:</label>
        <UiFormSelect id="year" value="2025" :options="[
          { id: 2021, name: '2021' },
          { id: 2022, name: '2022' },
          { id: 2023, name: '2023' },
          { id: 2024, name: '2024' },
          { id: 2025, name: '2025' }
        ]" />
      </div>
      <div class="ms-2">
        <label for="month" class="mr-2">Mes:</label>
        <UiFormSelect id="month" value="9" :options="[
          { id: 1, name: 'Enero' },
          { id: 2, name: 'Febrero' },
          { id: 3, name: 'Marzo' },
          { id: 4, name: 'Abril' },
          { id: 5, name: 'Mayo' },
          { id: 6, name: 'Junio' },
          { id: 7, name: 'Julio' },
          { id: 8, name: 'Agosto' },
          { id: 9, name: 'Septiembre' },
          { id: 10, name: 'Octubre' },
          { id: 11, name: 'Noviembre' },
          { id: 12, name: 'Diciembre' }
        ]" />
      </div>
      <div class="ms-2">
        <button class="border border-slate-400 text-red-500 px-4 py-2 mt-6 rounded">
          <i class="mdi mdi-filter"></i>
          Filtrar
        </button>
      </div>
    </UiCard>

    <UiCard>
      <UiTable :headers="[
        { label: 'Cliente', name: 'client'},
        { label: 'Fideicomiso', name: 'trust'},
        { label: 'Fic', name: 'fic'},
        { label: 'Año', name: 'year', classes: 'w-32'},
        { label: 'Mes', name: 'month'},
        { label: 'Documento', name: 'category'},
        { label: 'Formato', name: 'format'},
        { label: 'Descargar', name: 'download'}
      ]" :data="[
        {
          client: 'Droni.co',
          trust: 'Fideicomiso prueba',
          fic: 'FIC-001',
          year: '2021',
          month: 'Octubre',
          category: 'Estado financiero con terceros',
          format: 'PDF',
          download: 'Descargar'
        },
        {
          client: 'Droni.co',
          trust: 'Fideicomiso prueba',
          fic: 'FIC-001',
          year: '2021',
          month: 'Octubre',
          category: 'Estado financiero sin terceros',
          format: 'PDF',
          download: 'Descargar'
        },
        {
          client: 'Droni.co',
          trust: 'Fideicomiso prueba',
          fic: 'FIC-001',
          year: '2021',
          month: 'Octubre',
          category: 'Balances de prueba',
          format: 'PDF',
          download: 'Descargar'
        }
      ]">
        <template #download="item">
          <button class="border border-red-500 text-red-500 px-2 py-1 rounded">
            <i class="mdi mdi-download"></i>
            Descargar
          </button>
        </template>
      </UiTable>
    </UiCard>
    
  </div>
</template>