<template>
  <v-card max-width="400" class=" mx-auto mt-10">
    <v-card-title>Login</v-card-title>

    <v-text-field prepend-icon="mdi-account" label="Login"></v-text-field>
    <v-text-field
      :type="isPasswordHidden ? 'password' : 'text'"
      prepend-icon="mdi-lock"
      :append-icon="isPasswordHidden ? 'mdi-eye-off' : 'mdi-eye'"
      @click:append="isPasswordHidden = !isPasswordHidden"
      label="Password"
    ></v-text-field>
    <v-card-actions>
      <v-btn color="info">Register</v-btn>
      <v-spacer></v-spacer>
      <v-btn color="success">Login</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      isPasswordHidden: true,
    };
  },
};
</script>

<style></style>
