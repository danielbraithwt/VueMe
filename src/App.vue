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
          icon: '../../static/mark-github.svg',
          url: '#',
        },
        {
          icon: '../../static/mail.svg',
          url: '#',
        },
        {
          icon: '../../static/file.svg',
          url: '#',
        }
      ],
      about: {
        aboutme: {
          image: 'http://placehold.it/500x250',
          text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        },
        experence: {
          image: 'http://placehold.it/500x250',
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
          image: 'http://placehold.it/500x250',
          text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        }
      },
      projects: [
        {
          image: 'http://placehold.it/500x250',
          name: 'Name',
          url: 'http://website.com',
          git: 'https://github.com/danielbraithwt',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        },
        {
          image: 'http://placehold.it/500x250',
          name: 'Name',
          url: 'http://website.com',
          git: 'https://github.com/danielbraithwt',
          description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
        },
        {
          image: 'http://placehold.it/500x250',
          name: 'Name',
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
html {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
  background-color: #F9F9F9;
}

body {
  margin: 0;
  padding: 0;
}

.Card {
  height: auto;
  padding-bottom: 20px;

  margin-left: 10px;
  margin-top: 10px;
  margin-right: 10px;
  margin-bottom: 40px;

  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  border-radius: 2px;
  background-color: white;
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

.u-title {
  /*font-size: 6vw;*/
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

@media (min-width: 767px) {.u-sm-hidden {
    display: none !important;
}}

@media (min-width: 767px) {.u-sm-show {
    display: block !important;
}}

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
    display: none;
  }

  .u-sm-show {
    display: block;
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
    display: none;
  }

  .u-md-show {
    display: block;
  }
}

.MasonryColumn-Item {
  position: relative;
  display: inline-block;

  break-inside: avoid;
  -webkit-column-break-inside: avoid;
}
</style>
