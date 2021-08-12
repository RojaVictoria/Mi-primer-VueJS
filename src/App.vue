<template>
  <div id="app">
    <table class="table">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Nombre</th>
          <th scope="col">Apellido</th>
          <th scope="col">RUT</th>
          <th scope="col">Nacimiento</th>
          <th scope="col">Edad</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(persona, $index) of personas" :key="$index">
          <td>{{ $index + 1}}</td>
          <td>{{ persona.nombre }}</td>
          <td>{{ persona.apellido }}</td>
          <td>{{ persona.rut }}</td>
          <td>{{ persona.nacimiento }}</td>
          <td>{{ persona.edad }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>


export default {
  name: "App",
  data: () => ({
    personas: [
      {
        nombre: "Bruno",
        apellido: "Díaz",
        rut: "6333666-6",
        nacimiento: "15-10-2014",
        edad: 7,
      },
      {
        nombre: "Miguel",
        apellido: "De la Cruz",
        rut: "8666888-8",
        nacimiento: "20-05-2019",
        edad: 2,
      },
      {
        nombre: "Alicia",
        apellido: "Díaz",
        rut: "5222555-5",
        nacimiento: "05-02-2013",
        edad: 8,
      },
    ],
  }),
};
</script>

<style></style>
