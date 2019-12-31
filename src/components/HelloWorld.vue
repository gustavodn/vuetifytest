<template>
    <div class="row">
        <div class="col-md-8 offset-md-2">              
                <v-toolbar color="blue">
                    <v-spacer></v-spacer>
                    <v-toolbar-title>Instalaciones</v-toolbar-title>                
                </v-toolbar>               
                <v-form v-model="valid">
                    <v-container>
                        <v-row>
                            <v-col cols="12" md="4">
                                <v-text-field
                                    v-model="firstname"
                                    :rules="nameRules"                                    
                                    label="Codigo de la instalacion"
                                    required
                                ></v-text-field>
                            </v-col>

                            <v-col cols="12" md="4">
                                <v-text-field
                                    v-model="lastname"
                                    :rules="nameRules"                                    
                                    label="Nombre de la instalacion"
                                    required
                                ></v-text-field>
                            </v-col>

                            <v-col cols="12" md="4">
                                <v-text-field
                                    v-model="email"
                                    :rules="emailRules"
                                    label="Municipio"
                                    required
                                ></v-text-field>
                            </v-col>
                        </v-row>
                         <v-row>
                             <v-col cols="12" md="4">
                                <v-text-field
                                    v-model="firstname"
                                    :rules="nameRules"                                    
                                    label="Provincia"
                                    required
                                ></v-text-field>
                            </v-col>

                            <v-col cols="12" md="4">
                                <v-text-field
                                    v-model="lastname"
                                    :rules="nameRules"                                    
                                    label="Gestor de Mantenimiento"
                                    required
                                ></v-text-field>
                            </v-col>

                            <v-col cols="12" md="4">
                                <v-text-field
                                    v-model="email"
                                    :rules="emailRules"
                                    label="Jefe de zona"
                                    required
                                ></v-text-field>
                            </v-col>                       
                        </v-row>
                        <v-row>
                             <v-btn                       
                                :disabled="!valid"
                                color="success"
                                class="mr-4"
                                @click="validate">
                                Filtrar
                            </v-btn>
                            <v-btn
                                color="default"
                                class="mr-4"
                                @click="reset">
                                Limpiar
                            </v-btn>
                        </v-row>
                    </v-container>                                                           
                </v-form>           
        </div>
        <div class="col-md-8 offset-md-2">
            <v-data-table
                :headers="headers"
                :items="desserts"
                :sort-by="['codigo', 'fat']"
                :sort-desc="[false, true]"
                multi-sort
                class="elevation-1"
            >
             <template v-slot:item.calories="{ name }">
            <v-chip :color="getColor(name.calories)" dark>{{ item.calories }}</v-chip>
            </template>
            </v-data-table>
        </div>
    </div>
</template>
<script>
  export default {
    data () {
      return {
        valid: true,
        headers: [
          {
            text: 'Actions',
            align: 'left',
            sortable: false,
            value: 'action', 
            class: 'verde'                              
          },
          { text: 'Codigo', value: 'codigo',  class: 'verde' },
          { text: 'Nombre', value: 'nombre',  class: 'verde' },
          { text: 'GM', value: 'gm',  class: 'verde' },
          { text: 'TM', value: 'tm',  class: 'verde' },
          { text: 'JZ', value: 'jz',  class: 'verde' },
          { text: 'EJ', value: 'ej',  class: 'verde' },
          { text: 'Direccion', value: 'direccion',  class: 'verde' },
          { text: 'Elementos', value: 'elementos',  class: 'verde' },
          { text: 'Ultima Transamision', value: 'ultima',  class: 'verde' },
        ],
        desserts: [
          {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
          {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
         
         {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
         
         {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
         
         {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
         
         {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
         
         {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
         
         {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
         
         {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          },
         
         {
            action: 'Actions',
            codigo: '001',
            nombre: 'Instalacion 1',
            'gm': 'GM',
            'tm': 'TM',
            'jz': 'TM',
            'ej': 'EJ',
            'direccion': 'Calle Av Paseo, Plaza de Instalacion 4',
            'elementos': '22',
            'ultima': '06/12/2019 19:18:57',       
          }                  
        ],
      }
    },
  }
</script>
<style >
    .verde{
        background-color: green;
    }
</style>
