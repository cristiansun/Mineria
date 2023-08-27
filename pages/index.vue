<template>
  <div>
    <h1 class="font-bold text-center italic text-3xl text-blue-400" padding:1 >Detección de movimientos</h1>
      <div class="flex lg:flex-row flex-col justify-center gap-x-6">
        <div class="p-2 ">
          <a-card class="hover:scale-105 transition-all border-gray-100"  style="width: 240px">
            <img
              slot="cover"
              alt="example"
              src="https://static.vecteezy.com/system/resources/previews/004/221/969/non_2x/dog-mascot-sitting-free-vector.jpg"
            />
            <a-card-meta class="text-center" title="Mascota sentada">
              <template slot="description">
                Movimiento a detectar
              </template>
            </a-card-meta>
          </a-card>
          
          <a-card class="hover:shadow-2xl hover:scale-105 transition-all" hoverable style="width: 240px">
            <img
              slot="cover"
              alt="example"
              src="https://img.freepik.com/vector-premium/perro-acostado-concepto-entrenamiento-mascotas-ilustracion-vectorial_605517-357.jpg?w=740"/>
            <a-card-meta class="text-center" title="Mascota acostada">
              <template slot="description">
                Movimiento a detectar
              </template>
            </a-card-meta>
          </a-card>
        </div>

        <div class="p-2">
          <Camara v-if="camaraVisible" @isStop="camaraVisible=false" />
          <a-card v-else>
          <a-card>
            <img
              slot="cover"
              alt="example"
              src="https://png.pngtree.com/png-vector/20220514/ourlarge/pngtree-camara-icon-design-png-image_4630479.png"
            />
          </a-card>
        </div>

        <div class="p-2 ">
          <a-card class="hover:shadow-2xl hover:scale-105 transition-all" hoverable style="width: 240px">
            <img
              slot="cover"
              alt="example"
              src="https://static.vecteezy.com/system/resources/previews/019/550/823/original/cartoon-illustration-of-a-jack-russell-terrier-the-dog-is-standing-sideways-with-head-raised-isolated-on-a-blue-background-pets-animals-dog-theme-a-design-element-in-a-flat-style-vector.jpg"
            />
            <a-card-meta class="text-center" title="Mascota quieta">
              <template slot="description">
                Movimiento a detectar
              </template>
            </a-card-meta>
          </a-card>
          
          <a-card class="hover:shadow-2xl hover:scale-105 transition-all" hoverable style="width: 240px">
            <img
              slot="cover"
              alt="example"
              src="https://static.vecteezy.com/system/resources/previews/007/637/359/non_2x/photo-camera-zone-black-silhouette-icon-notice-photography-allowed-area-alert-camera-capture-zone-place-red-green-circle-symbol-no-photograph-camera-sign-isolated-illustration-vector.jpg"/>
            <a-card-meta class="text-center text-2xl" title="Orden detectada">
              <template slot="description">
                <h1 class="text-green-500">
                Orden detectada
              </h1>
              </template>
             
            </a-card-meta>
          </a-card>
        </div>
      </div>
      <a-button @click="camaraVisible=true">Encender camara</a-button> 

      </div>  

  </div>
</template>

<script>
import moment from 'moment'
import Camara from '../components/camara.vue'
export default {
  components: {
    Camara,
  },
  layout: 'home',
  name: 'IndexPage',
  data() {
    return {
      camaraVisible: false,
    }
  },
  head() {
    return {
      title: 'Tareas'
    }
  },
  methods: {
    mostrar(message) {
      console.log(message)
    },
    detener() {
      console.log("se envio a detener")
      this.camaraVisible = false
    },
  }
}
</script>