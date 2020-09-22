<template>
  <div>
    <v-app-bar app color="primary" dense dark>
      <v-app-bar-nav-icon @click="HideClickMenu"></v-app-bar-nav-icon>

      <v-toolbar-title>{{title}} V{{ version }}</v-toolbar-title>

      <v-spacer></v-spacer>
      <span>{{$store.getters["username"] }}</span>
      <v-btn icon>
        <v-icon  @click="onClickLogOff">mdi-export</v-icon>
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Header",
  computed: {
    version() {
      return "1.0";
    },
    title() {
      return "AIDaily";
    }
  },
  methods: {
    HideClickMenu() {
      if (this.$store.state.Hide == false) {
        this.$store.state.Hide = true;
      } else {
        this.$store.state.Hide = false;
      }
    },
    onClickLogOff() {
      this.$router.push("/");
      this.$store.dispatch("doLogout");
    }
  }
};
</script>

<style>
</style>