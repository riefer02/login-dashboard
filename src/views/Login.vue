<template>
  <!-- Login Module -->
  <v-card width="400px" class="mx-auto mt-10"
    ><v-card-title>
      <h1 class="display-1">Login</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field
          label="Username"
          prepend-icon="mdi-account-circle"
        ></v-text-field>
        <v-text-field
          :type="showPassword ? 'true' : 'password'"
          @click:append="showPassword = !showPassword"
          label="Password"
          prepend-icon="mdi-lock"
          :append-icon="showPassword ? 'mdi-eye ' : 'mdi-eye-off'"
        ></v-text-field>
      </v-form>
    </v-card-text>
    <v-divider></v-divider>
    <v-card-actions>
      <v-btn color="success">Register</v-btn>
      <v-spacer></v-spacer>
      <v-btn color="info">Login</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      showPassword: false,
    };
  },
};
</script>

<style lang="scss" scoped></style>
