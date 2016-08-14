<template>
  <div id="app">
    <header-section :name="name" :photo="photo" :social="social"></header-section>
    <about-section :about="about"></about-section>
    <project-section :projects="projects"></project-section>
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue';
import AboutSection from './components/AboutSection.vue';
import ProjectSection from './components/ProjectSection.vue';

export default {
  name: 'app',
  components: {
    HeaderSection,
    AboutSection,
    ProjectSection
  },
  data: function() {
    return {
      name: "Daniel Braithwaite",
      photo: "../../static/profile-photo.jpg",
      social: [
        {
          name: 'Github',
          label: 'Github Link Clicked',
          icon: '../../static/mark-github.svg',
          url: 'https://github.com/danielbraithwt',
        },
        {
          name: 'Email',
          label: 'Email Link Clicked',
          icon: '../../static/mail.svg',
          url: '#',
        },
        {
          name: 'Resume',
          label: 'Resume Link Clicked',
          icon: '../../static/file.svg',
          url: '#',
        }
      ],
      about: {
        aboutme: {
          image: '../static/About-profile_02.png',
          subtitle: 'What makes me Daniel',
          text: "I'm a caffeine-addicted, fitness-loving nerd who thrives on writing code and solving difficult problems. My passion started with design, but after learning C with my dad I fell in love with the art of programming. I love being able to affect and enhance people's lives by creating beautiful and useful software.",
        },
        experence: {
          image: '../static/About-work_02.png',
          subtitle: 'What I have done',
          text: "During my second year of study I was lucky enough to get an internship at the amazing Wellington company Alphero as a web developer. Alphero has some incredible designers and takes pride in creating beautiful web and mobile apps. As a developer I loved being a part of this environment. This opportunity allowed me work on a lot of projects using a wide range of cutting edge technologies.",
          skills: [
            {
              name: 'JS',
              color: 'yellow'
            },
            {
              name: 'Ember',
              color: 'amber'
            }
          ]
        },
        quallifications: {
          image: '../static/About-quall_02.png',
          subtitle: 'What got me to where I am',
          text: "My passion started at high school, where I had three amazing teachers and two supportive parents giving me the opportunities to achieve highly in the fields that I love. I'm now at Victoria University of Wellington where I'm in my third and final year of my BSc in Computer Science and Mathematics."
        },
        interests: {
          image: 'http://placehold.it/500x250',
          subtitle: 'What are my interests',
          text: "After taking an Introduction to Artificial Intelligence and a Algorithm Design paper at my university I found that these two topics really interested me. I particularly enjoyed being able to use AI techniques with a large collection of data to produce meaningful information from it. The algorithm design course involved taking problems and using different techniques to solve them and then prove our algorithms were correct. Proving algorithms correct particularly appealed to me as most of the course I took were not this rigorous or mathematical."
        }
      },
      projects: [
        {
          image: 'http://placehold.it/500x250',
          name: 'Cooperative Bank',
          subtitle: 'Alphero',
          url: 'https://www.co-operativebank.co.nz/',
          // git: '',
          description: "This was an Ember JS project. I was responsible for making upgrades and bug fixes along with helping build the overdraft flow",
        },
        {
          image: 'http://placehold.it/500x250',
          name: 'Paymark',
          subtitle: 'Alphero',
          url: 'https://www.paymark.co.nz/',
          // git: '',
          description: "For this website we used Webhook CMS to load our content and then plain JS and SASS. This was one of my favorite projects i have worked on as this was the first industry project I was able to take from start to finish (mostly the summer was over before the site went live).",
        },
        {
          image: 'http://placehold.it/500x250',
          name: 'Lighthouse Chromecast Reciver',
          subtitle: 'Alphero',
          // url: '',
          // git: '',
          description: "I was responsible for creating the Chromecast receiver application for Lighthouse (a tv/movie streaming service). ",
        },
        {
          image: 'http://placehold.it/500x250',
          name: 'VueMe',
          subtitle: 'Personal',
          url: 'danielbraithwaite.name',
          git: 'https://github.com/danielbraithwt/VueMe',
          description: "After learning so much at Alphero I wanted a way to apply what I had learnt, remaking my personal website seemed like a natural way to apply these skills. The current JS frameworks I knew didn't seem like a good fit so this was an opportunity to learn a new front end framework. I chose Vue because of its simplicity, which was good because there wasn't a huge learning curve for the framework, also Vue is much less opinionated than other frameworks allowing me to structure the project how I wanted.",
        },
        {
          image: 'http://placehold.it/500x250',
          name: 'Whats Next',
          subtitle: 'GovHack 2016 - Personal',
          // url: '',
          git: 'https://github.com/working-title/whats-next',
          description: "What's next was created at GovHack 2015 and was designed to help high school leavers make informed decisions about what to do next. Often there is a lot of pressure on school leavers from family, friends or teachers  to go to university or learn a trade, this can make deciding what is best for you even more difficult than it already is. What's next allows school leavers to compare a number of creators based on a number of different factors so they can make an informed choice about what's next.",
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import './styles/index.scss';
</style>
