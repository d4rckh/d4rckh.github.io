<template>
  <v-app>
      <v-app-bar
        color="dark"
      >
        <v-app-bar-title>d4rckh</v-app-bar-title>
        <template v-slot:append>
          <v-btn icon="mdi-post" link href="https://d4rckh.github.io/blog"></v-btn>
          <v-btn icon="mdi-twitter" link href="https://twitter.com/d4rckh"></v-btn>
          <v-btn icon="mdi-github" link href="https://github.com/d4rckh"></v-btn>
          <v-btn icon="mdi-patreon" link href="https://patreon.com/d4rckh"></v-btn>
        </template>

      </v-app-bar>

    <v-main>
      <div class="d-flex flex-column justify-center align-center">
        <h1 class="text-h2 mt-10">
          d4rckh
        </h1>
      </div>
      <div class="d-flex flex-column justify-center align-center">
        <h1 class="text-h4 mt-10">
          Projects
        </h1>
      </div>
      <v-row style="margin:auto"  class="mt-5" justify="center">
        <v-col md="3">
          <ProjectCard 
            title="nimc2" 
            description="lightweight c2 written fully in nim" 
            link="http://github.com/d4rckh/nimc2"
            pic="https://user-images.githubusercontent.com/35298550/167257694-1cda7f5c-a013-4910-af93-f51ad1d6ca4a.png"
            longDescription="nimc2 is a very lightweight C2 written fully in nim (implant & server). If you want to give it a try check out the wiki to learn how to install and use nimc2. It's features include Windows and Linux implant generation, TCP socket communication, ability to create as many listeners as you want, a nice task system, an easy to use CLI and a lot more."
          />
        </v-col>
        <v-col md="3">
          <ProjectCard 
            title="vaf" 
            description="cross-platform very advanced and fast web fuzzer written in nim" 
            link="https://github.com/d4rckh/vaf"
            pic="https://github.com/d4rckh/vaf/raw/main/screenshots/main.png"
            longDescription="vaf is a cross-platform web fuzzer with a lot of features. Some of its features include fast threading, http header fuzzing, proxying and much more."
          />
        </v-col>
        <v-col md="3">
          <ProjectCard 
            title="Red Team Techniques" 
            description="Active Directory attacks explained along with guides for configuring labs for performing the attacks" 
            link="https://redteamtechniques.github.io/"
            pic="https://media.discordapp.net/attachments/866042879619891231/980463841999745134/unknown.png"
            longDescription="This is a website made together with a friend (Enox) in which we explain different techniques for attacking active directory networks and more."
          />
        </v-col>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>

import ProjectCard from "./components/projectCard.vue"

export default {
  name: 'App',

  components: { ProjectCard },

  data: () => ({
    //
  }),
}
</script>
