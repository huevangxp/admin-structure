<template>
  <div>
    <v-row>
      <v-col cols="12" md="6">
        <v-card elevation="2" width="100%" height="300px">
          <v-card-title >
            Dashboard
          </v-card-title>
        </v-card>
        <v-card class="mt-1" elevation="2" width="100%" height="300px">
          <v-card-title >
            Total Orders
          </v-card-title>
        </v-card>
      </v-col>
      <v-col cols="12" md="3">
        <v-card   elevation="2" width="100%" height="300px">
          <v-card-title >
            Payments
          </v-card-title>
        </v-card>
        <v-card class="mt-5" elevation="2" width="100%" height="280px">
          <v-card-title >
            Latest Deal
          </v-card-title>
        </v-card>
      </v-col>
      <v-col cols="12" md="3">
        <v-card  elevation="2" width="100%" height="300px">
          <v-card-title >
            Products
          </v-card-title>
        </v-card>
        <v-card  class="mt-5"  elevation="2" width="100%" height="280px">
          <v-card-title >
            Customers
          </v-card-title>
        </v-card>
      </v-col>
<v-col cols="12" md="8">
  <v-card  class="mt-5"  elevation="2" width="100%" height="400px">
    <v-card-title >
      table product
    </v-card-title>
  </v-card>
</v-col>
<v-col cols="12" md="4">
  <v-card  class="mt-5"  elevation="2" width="100%" height="400px">
    <v-card-title >
      Test
    </v-card-title>
  </v-card>
</v-col>
      <v-col cols="12">
        <v-card  class="mt-5"  elevation="2" width="100%" height="400px">
          <v-card-title >
            Latest reviews
          </v-card-title>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>
