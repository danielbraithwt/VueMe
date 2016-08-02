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

<style>
@font-face {
  font-family: Roboto;
  src: url(../static/fonts/Roboto-Regular.ttf);
}

@font-face {
  font-family: Roboto;
  src: url(../static/fonts/Roboto-Bold.ttf);
  font-weight: bold;
}

@font-face {
  font-family: Roboto;
  src: url(../static/fonts/Roboto-Medium.ttf);
  font-weight: 500;
}

html {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
  background-color: #F9F9F9;

  font-family: Roboto;
}

body {
  margin: 0;
  padding: 0;
}

.Title {
  font-weight: bold;
  text-transform: capitalize;
  font-size: 5em;
  margin-top: 0.5em;
  margin-bottom: 0.5em;
}

.Fill {
  height: 100%;
  width: 100%;
}

.Fill--height {
  min-height: 100vh;
}

.Fill--width {
  width: 100vw;
}

.Container {
  max-width: 96%;
  margin-left: 2%;
  margin-right: 2%;
}

.u-background {
  /*width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  z-index: -2;*/

  background-color: #2196F3;
}

.u-textWhite {
  color: white;
}

.u-p-0 {
  padding: 0;
}

.u-mB-sm {
  margin-bottom: 10px;
}

.u-mB-md {
  margin-bottom: 15px;
}

.u-mB-lg {
  margin-bottom: 20px;
}

.u-xs-hide {
  display: none;
}

.u-xs-show {
  display: block;
}

.MasonryColumn {
  position: relative;
  -webkit-perspective: 1px;
  perspective: 1px;
  column-count: 1;
}

.MasonryColumn--balanced {
  column-fill: balance;
}

@media only screen and (min-width: 48em) {
  .MasonryColumn {
    column-count: 2;
  }

  .u-sm-hide {
    display: none !important;
  }

  .u-sm-show {
    display: block !important;
  }

  .u-sm-mh-0 {
    min-height: 0px !important;
  }
}

@media only screen and (min-width: 62em) {
  .MasonryColumn {
    column-count: 3;
  }

  .u-md-hide {
    display: none !important;
  }

  .u-md-show {
    display: block !important;
  }
}

.MasonryColumn-Item {
  position: relative;
  display: inline-block;

  break-inside: avoid;
  -webkit-column-break-inside: avoid;
}

.Ripple::after {
  content: '';
  display: block;
  position: absolute;
  left: 50%;
  top: 50%;
  width: 120px;
  height: 120px;

  background-color: #E0E0E0;

  margin-left: -60px;
  margin-top: -60px;

  border-radius: 100%;
  opacity: 0.6;

  transform: scale(0);
}

.Ripple:hover::after {
  animation: ripple 1s ease-out;
}

.Ripple:active::after {
    animation: ripple 1s ease-out;
}

@keyframes ripple {
  0% {
    transform: scale(0);
  }
  20% {
    transform: scale(1);
  }
  100% {
    opacity: 0;
    transform: scale(1);
  }
}

</style>
