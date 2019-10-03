<template>
  <v-app style="background:#efefef">
    <!-- <v-navigation-drawer v-model="drawer" absolute right temporary color="black">
      <v-list nav dense>
        <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
          <v-list-item>
            <v-list-item-title>Foo</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Bar</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Fizz</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title>Buzz</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>-->

    <v-content>
      <HelloWorld />
    </v-content>
    <v-footer class="white" padless>
      <v-container>
        <v-card class="flex" flat tile>
          <!-- <v-card-title class="white"></v-card-title> -->
          <v-layout>
            <v-flex md2>
              <ul>
                <li class="heading">INFO</li>
                <br />
                <li>About</li>
                <li>Journal</li>
                <li>Contact</li>
              </ul>
            </v-flex>
            <v-flex md2>
              <ul>
                <li class="heading">CATEGORIES</li>
                <br />
                <li>Wood</li>
                <li>Fashion</li>
                <li>UX Stuff</li>
              </ul>
            </v-flex>
            <v-flex md2>
              <ul>
                <li class="heading">FOLLOW</li>
                <br />
                <li style="color: blue">Facebook</li>
                <li>Instagram</li>
                <li style="color:teal">Twitter</li>
                <li style="color:red">Pinterest</li>
              </ul>
            </v-flex>
          </v-layout>
        </v-card>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld
  },
  data: () => ({
    drawer: false,
    group: null
  }),
  watch: {
    group() {
      this.drawer = false;
    }
  }
};
</script>
<style  scoped>
ul {
  list-style-type: none;
}

.heading {
  font-family: "Courier New", Courier, monospace;
  color: #aca9a9;
}
</style>