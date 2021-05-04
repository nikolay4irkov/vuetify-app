<template>
  <div>
    <v-container>
      <v-row>
        <v-col cols="4">
          <h1>Signup</h1>
          <v-form @submit.prevent="submit" class="mx-auto">
            <v-text-field label="Email"></v-text-field>
            <v-autocomplete
              :items="browsers"
              label="Choose your browser"
            ></v-autocomplete>
            <v-file-input
              show-size=""
              label="Upload your photo"
              truncate-length="15"
            ></v-file-input>
            <v-text-field
              label="Birthday"
              readonly
              v-model="birthday"
            ></v-text-field>
            <v-date-picker v-model="birthday"></v-date-picker>
            <v-checkbox label="I agree to Terms&Conditions"></v-checkbox>
            <v-btn color="primary" type="submit">Submit</v-btn>
          </v-form>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      browsers: ["Chrome", "Mozilla", "Safari"],
      birthday: "",
    };
  },
  methods: {
    submit() {
      alert(this.birthday);
    },
  },
};
</script>

<style></style>
