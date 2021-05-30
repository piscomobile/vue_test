
<template>
  <div>
    <v-text-field
      v-model="nombre"
      append-icon="mdi-book"
      :label="nombre"
      single-line
      hide-details
      clearable
      id="nombre"
      clear-icon="mdi-close"
    />
    <v-text-field
      v-model="apellido"
      append-icon="mdi-magnify"
      :label="apellido"
      single-line
      hide-details
      clearable
      id="apellido"
      clear-icon="mdi-close"
    />

    <div class="developer__metadata">{{ metadata }}</div>
  </div>
</template>

<script>
export default {
  
  props:{
    leyenda:String
  },
  data: function () {
    return {
      count: 0,
      nombre: "",
      apellido: "",
    };
  },
  computed: {
    metadata() {
       let meta= `${this.leyenda} ${this.nombre} ${this.apellido}`
       return meta
    },
  },
};
</script>