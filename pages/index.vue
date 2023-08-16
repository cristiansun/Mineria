<template>
  <div >
    <h1 class="font-bold text-3xl" padding:1 >Detección de movimientos</h1>
      <a-card hoverable style="width: 240px">
      <img
        slot="cover"
        alt="example"
        src="https://static.vecteezy.com/system/resources/previews/004/221/969/non_2x/dog-mascot-sitting-free-vector.jpg"
      />
      <a-card-meta title="Mascota sentada">
        <template slot="description">
          Movimiento a detectar
        </template>
      </a-card-meta>
      </a-card>
      
      <a-card hoverable style="width: 240px">
      <img
        slot="cover"
        alt="example"
        src="https://img.freepik.com/vector-premium/perro-acostado-concepto-entrenamiento-mascotas-ilustracion-vectorial_605517-357.jpg?w=740"/>
      <a-card-meta title="Mascota acostada">
        <template slot="description">
          Movimiento a detectar
        </template>
      </a-card-meta>
      </a-card>
  </div>
</template>

<script>
import moment from 'moment'
export default {
  layout: 'home',
  name: 'IndexPage',
  data() {
    return {
    }
  },
  head() {
    return {
      title: 'Tareas'
    }
  },
}
</script>
