<template>
  <v-app>
    <v-container>
      <v-card v-ripple v-resize="onResize">
        <div style="text-align: center">
          <v-img src="@/vuetify.png" style="display: inline-flex"></v-img>
        </div>
        <v-card-text>
          <v-text-field></v-text-field>
        </v-card-text>
      </v-card>
      <v-card v-bind="$attrs" v-ripple>v-bind</v-card>
      <v-card v-on="$listeners" v-ripple>v-on</v-card>
      <v-card v-bind="$attrs" v-on="$listeners" v-ripple>v-bind v-on</v-card>
      <pre>{{ {
        directives: [{
          name: "resize"
        }]
      } }}</pre>
      <setup-component />
    </v-container>
  </v-app>
</template>

<script>
  import SetupComponent from './Setup.vue'
  const img = require('@/vuetify.png?vuetify-preload')
  console.log(img, img.default)
  export default {
    components: {
      SetupComponent
    }
  }
</script>
