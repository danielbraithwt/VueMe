<template>
  <div id="app">
    <header-section :name="name" :photo="photo" :social="social"></header-section>
    <about-section :about="about"></about-section>
    <research-section :research="research"></research-section>
    <project-section :projects="projects"></project-section>
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue';
import AboutSection from './components/AboutSection.vue';
import ProjectSection from './components/ProjectSection.vue';
import ResearchSection from './components/ResearchSection.vue';

export default {
  name: 'app',
  components: {
    HeaderSection,
    AboutSection,
    ProjectSection,
    ResearchSection,
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
          url: 'mailto:danielbraithwt@gmail.com',
        },
        {
          name: 'Resume',
          label: 'Resume Link Clicked',
          icon: '../../static/file.svg',
          url: '../static/Resume.pdf',
        }
      ],
      about: {
        aboutme: {
          image: '../static/About-Me.png',
          subtitle: 'What makes me Daniel',
          text: "I'm a caffeine-addicted, fitness-loving nerd who thrives on solving interesting and difficult problems. My passion started with design, but after learning C with my dad I fell in love with the art of programming. My interestes have sinse shifted from simply enjoying programming to seeking a more mathematical understanding of how things work.",
        },
        experence: {
          image: '../static/About-Work.png',
          subtitle: 'What I have done',
          text: "During my second year of study I was lucky enough to get an internship at the amazing Wellington company Alphero as a web developer. Alphero has some incredible designers and takes pride in creating beautiful web and mobile apps. As a developer I loved being a part of this environment. This opportunity allowed me work on a lot of projects using a wide range of cutting edge technologies.",
          //skills: [
          //  {
          //    name: 'JS',
          //    color: 'yellow'
          //  },
          //  {
          //    name: 'Ember',
          //    color: 'amber'
          //  }
          //]
        },
        quallifications: {
          image: '../static/About-Qull.png',
          subtitle: 'What got me to where I am',
          text: "My passion started at high school, where I had three amazing teachers and two supportive parents giving me the opportunities to achieve highly in the fields that I love. I'm now at Victoria University of Wellington where I have finished my BSc in Computer Science and Mathematics and am pursuing a BSc with Honors in the same fields. Following this I am interested in doing further postgraduate study."
        },
        interests: {
          image: '../static/About-interests.png',
          subtitle: 'What are my interests',
          text: "I am very interested in Machine Learning and as part of my honors degree I am able to persue research into areas of machine learning which I find interesting. One such area is Logical Neural Netowrks, this is a Neural Network where the activations are 'Noisy' logic gates. The idea of using these activation functions is to yield trained networks that are more interpretable so that someone might analyze what features the network has learnt. Outside of study I love to be moving and exercising, I am training to compete in Olympic Weightlifting."
        }
      },
      projects: [
        {
          // image: 'http://placehold.it/500x250',
          name: 'NZ Banking Website',
          subtitle: 'Alphero',
          description: "This was an Ember JS project for a New Zealand bank. I was responsible for making upgrades and bug fixes along with helping build the overdraft flow. This project allowed me to develop a good understanding of EmberJS but also working in a team.",
        },
        {
          // image: 'http://placehold.it/500x250',
          name: 'Large NZ Eftpos Retailer',
          subtitle: 'Alphero',
          description: "For this website we used Webhook CMS to load our content and then plain JS and SASS. This was one of my favorite projects I have worked on as this was the first industry project I was able to take from start to finish (mostly the summer was over before the site went live).",
        },
        {
          // image: 'http://placehold.it/500x250',
          name: 'NZ Streaming Service Chromecast Reciver',
          subtitle: 'Alphero',
          description: "I was responsible for working on the Chromecast Receiver application for an NZ TV/Movie streaming service. Working on the communication between android app and receiver as well as the interface.",
        },
        {
          // image: 'http://placehold.it/500x250',
          name: 'VueMe',
          subtitle: 'Personal',
          url: 'danielbraithwaite.name',
          git: 'https://github.com/danielbraithwt/VueMe',
          description: "After learning so much at Alphero I wanted a way to apply what I had learnt, remaking my personal website seemed like a natural way to apply these skills. The current JS frameworks I knew didn't seem like a good fit so this was an opportunity to learn a new front end framework. I chose Vue because of its simplicity, which was good because there wasn't a huge learning curve for the framework, also Vue is much less opinionated than other frameworks allowing me to structure the project how I wanted.",
        },
        {
          // image: 'http://placehold.it/500x250',
          name: 'Whats Next',
          subtitle: 'GovHack 2016 - Personal',
          // url: '',
          git: 'https://github.com/working-title/whats-next',
          description: "What's next was created at GovHack 2015 and was designed to help high school leavers make informed decisions about what to do next. Often there is a lot of pressure on school leavers from family, friends or teachers  to go to university or learn a trade, this can make deciding what is best for you even more difficult than it already is. What's next allows school leavers to compare a number of creators based on a number of different factors so they can make an informed choice about what's next.",
        }
      ],
      research: [
        {
          name: 'Logical Neural Networks: Opening the black box',
          description: 'Logical neural networks are networks built with neurons using activation functions based off logical gates. I am continuing on from research done by a previous honos student who gave a proof of concept for Logical Neural Netowrks, they where shown to provide reasonable accuraccy and to be alot more understandble as oposed to networks using regular activation functions. I am continuing this research by first showing we can use Logical Nets to learn Boolean expressions. Currently there only OR and AND neurons which when combined arnt functionally complete so I will implement other gates such as NAND.',
          git: 'https://github.com/danielbraithwt/Logical-Neural-Networks',
        },
        {
          name: 'Machine Learning of Collectives of local decision makers',
          description: 'The idea behind this research project is to create nerons which rather than being tightly connected they are as seperate as possible to allow adding and removal of neurons. Training will involve nurons identifying some part of the data which is "interesting" and learn to classify that area of the data.',
          git: 'https://github.com/garibaldu/boundary-seekers',
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import './styles/index.scss';
</style>
