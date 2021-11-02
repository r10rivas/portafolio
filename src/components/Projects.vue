<template>
  <section class="min-h-screen p-12 flex flex-col text-app-white bg-app-black
                  sm:px-20
                  lg:p0 lg:items-center lg:justify-center"
  >
    <div class="w-full
                lg:w-4/5"
    >
      <h1 class="mt-8 mb-20 text-3xl text-center font-bold
                 md:text-4xl
                 lg:text-5xl"
      >
        Projects
      </h1>

      <ListProjects :projectsData="projects"/>

    </div>
  </section>
</template>

<script>
  import GitHubIcon from "./../assets/images/github-icon.svg";
  import ExternalLinkIcon from "./../assets/images/external-link-icon.svg";
  import Pokehack from "./../assets/images/projects/pokehack.gif";
  import WeatherApp from "./../assets/images/projects/weather-app.gif";
  import FoxesVsRabbits from "./../assets/images/projects/foxes-vs-rabbits.gif";
  import TodoListApp from "./../assets/images/projects/todo-list-app.gif";

  import ListProjects from "./ListProjects";

  export default {
    name: "Projects",
    data: function () {
      return {
        GitHubIcon: GitHubIcon,
        ExternalLinkIcon: ExternalLinkIcon,
        Pokehack: Pokehack,

        projects: [
          {
            name: "Pokehack",
            description: "A simple SPA that allows you to view a list of pokemons, view pokemon features, save your favorite pokemon.",
            technologies: ['Vuejs 2, TailwindCSS'],
            linkGitHub: "https://github.com/r10rivas/pokehack-vue",
            linkProject: "https://pokehack.netlify.app/",
            image: Pokehack,
          },
          {
            name: "Weather App",
            description: "Application to know the climate of different countries",
            technologies: ['Vuejs 2, TailwindCSS'],
            linkGitHub: "https://github.com/r10rivas/weather-app-vue",
            linkProject: "https://r10rivas-weather-app.netlify.app/",
            image: WeatherApp,
          },
          {
            name: "Foxes Vs Rabbits",
            description: "Foxes vs Rabbits is a challenge/game aimed at demonstrating the skills and knowledge acquired on programming.",
            technologies: ['ruby'],
            linkGitHub: "https://github.com/r10rivas/foxes-vs-rabbits",
            image: FoxesVsRabbits,
          },
          {
            name: "Todo List App",
            description: "The classic todo app with a few twists! This app includes a dark/light theme toggle.",
            technologies: ['Vuejs 3', 'TailwindCSS'],
            linkGitHub: "https://github.com/r10rivas/todo-list-app-vue",
            linkProject: "https://todo-list-app-vue-m3u77uj3v-r10rivas.vercel.app/",
            image: TodoListApp,
          },
        ]
      }
    },
    components: {
      ListProjects
    },
  }
</script>
