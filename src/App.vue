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
          url: '#',
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
          text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        },
        experence: {
          image: '../static/About-work_02.png',
          text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
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
          text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        }
      },
      projects: [
        {
          image: 'http://placehold.it/500x250',
          name: 'Name',
          subtitle: 'Subtitle',
          url: 'http://website.com',
          git: 'https://github.com/danielbraithwt',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        },
        {
          image: 'http://placehold.it/500x250',
          name: 'Name',
          subtitle: 'Subtitle',
          url: 'http://website.com',
          git: 'https://github.com/danielbraithwt',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        },
        {
          image: 'http://placehold.it/500x250',
          name: 'Name',
          subtitle: 'Subtitle',
          url: 'http://website.com',
          git: 'https://github.com/danielbraithwt',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import './styles/index.scss';
</style>
