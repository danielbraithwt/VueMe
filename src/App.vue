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
      photo: "data:image/jpeg;base64,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",
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
