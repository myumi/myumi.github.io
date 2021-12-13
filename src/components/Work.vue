<template>
  <section id="work">
    <div class="work__headers">
      <h1 class="headers__h1 headers__h1--highlight">Work</h1>
      <h2 class="headers__h2">These are some projects I've left my mark on.</h2>
    </div>
    <div class="work--projects">
      <WorkItem
        v-for="project in projects"
        :key="project.title"
        :image="project.image"
        :imageAlt="project.imageAlt"
        :label="project.label"
        :title="project.title"
        :tools="project.tools"
        :description="project.description"
        :recognitions="project.recognitions"
        :github="project.github"
      />
    </div>
  </section>
</template>

<script>
import WorkItem from './WorkItem.vue'

export default {
  components: {
    WorkItem 
  },
  data() {
    return {
      projects: [
        {
          image: 'https://images.unsplash.com/photo-1519750783826-e2420f4d687f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTJ8fGJva2VofGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
          imageAlt: `A snapshot of a website that emulates the pattern-making tool 
            in the Nintendo Switch game Animal Crossing: New Horizions`,
          label: 'Web App',
          title: 'ACPatterns',
          tools: ['Vue', 'SCSS'],
          description: `<p>I worked alongside two other developers to develop and design an 
            application that supports a community with tens of millions of users.</p>
            <p>This project was built in Vue, integrating and updating a similar tool
            one of the other developers had worked on, as well as a version of the ZXing library by Google I modified to support our needs.</p>
            <p>As well as development, my responsibilites included moderating the Discord community for the project as well as answering user questions and
            applying changes and fixes to suite the ever-changing needs of the community.</p>`,
          recognitions: [
            {
              type: 'Featured',
              names: ['Wall Street Journal', 'Kotaku', 'Polygon', 'Washington Post'],
            },
            {
              type: 'Forked',
              names: ['Getty Museum', 'the Metropolitan Museum of Art', 'Jackbox Games'],
            },
            {
              type: 'Used',
              names: ['the Joe Biden Campaign', 'and more'],
            },
          ],
          github: 'https://github.com/Thulinma/ACNLPatternTool',
        },
        {
          image: 'https://images.unsplash.com/photo-1519750783826-e2420f4d687f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTJ8fGJva2VofGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
          imageAlt: `A snapshot of a website that emulates the pattern-making tool 
            in the Nintendo Switch game Animal Crossing: New Horizions`,
          label: 'Web App and Design',
          title: 'Guardian',
          tools: ['React', 'TypeScript', 'Google Cloud Platform', 'SCSS', 'Figma'],
          description: `<p>I like niche things. If a subculture exists, I am probably going to fall into it. One of those things is pet sims.</p>
          <p>I started playing Flight Rising back in college, but as the 2019-2X COVID pandemic kicked in, I needed something to distract myself with. 
          I started playng Flight Rising again with a group of friends and found a few gaps in supporting tools for the game. Although various sites, Google sheets, 
          and forum posts existed as guides, there was no central hub that had it all.</p>
          <p>I made Guardian, named after a popular dragon breed on the site, to satisfy the helper tools I found myself needing while I played.</p>`,
          github: 'https://github.com/myumi/guardian',
        },
        {
          image: 'https://images.unsplash.com/photo-1519750783826-e2420f4d687f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTJ8fGJva2VofGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
          imageAlt: '',
          label: 'Dicord Bot',
          title: 'Elder Drake',
          tools: ['TypeScript', 'Discord API', 'Express', 'Heroku'],
          description: `<p>I started playing the game League of Legends when I was in college. (No, I'm not good.) 
          It was great for stress-relief in between classes and was a wonderful way to stay in touch with my friends over the summers.
          Over the pandemic, we picked it up again as a background for talking with each other over Discord.</p>
          <p>The game is constantly updating and changing. Many of us were getting back into it, and constantly needing to look up specific information. There is no exisiting or currently-maintained Discord bot to do so. So, I made one, and after suffering through the offical API's format and inaccurate information, I quickly discovered why one didn't already exist.</p>
          <p>However, it's in a working state. Currently, I'm working with another developer friend to build <a href="https://github.com/myumi/elder-drake-api">a middleman API service</a> for the bot so it doesn't have to do as much parsing and object traversing as it currently does, as well as try to format the data to be more consistent.`,
          github: 'https://github.com/myumi/elder-drake',
        },
        {
          image: 'https://images.unsplash.com/photo-1519750783826-e2420f4d687f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTJ8fGJva2VofGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
          imageAlt: `A collection of designs and mockups`,
          label: 'Web apps and design',
          title: 'Vibrant Emotional Health',
          tools: ['React', 'Gatsby', 'Vue', 'Cypress', 'SCSS', 'Figma'],
          description: `
            <p>Working with Vibrant was an interesting experience, as the development team was small and we had a lot of freedom in the tools we used to to work. I was able to contribute, if not completely develop and design, products that had a very large user base.</p>
            <p>I developed the new web-based chat platform for the National Suicide Hotline, integrating a contracted third-party chat service.</p>
            <p>I designed the interface for a new system in Figma and built it out in Vue, React, and Gatsby.</p>
            <p>Working closely with experts in the mental health field, I was often the communication between the tech department and stakeholders, making sure both felt heard and understood.</p>`,
        },
      ]
    }
  }
}
</script>

<style lang="scss">
  @import '../sass/main.scss';

  #work {
    display: flex;
    flex-direction: column;
    align-items: center;

    margin: 40px auto ;
    min-height: 600px;

    @include desktop {
      width: 1100px;
    }
  }

  .work__headers {
    width: 100%;
  }

  .headers__h1 {
    display: inline;
    font-size: 28px;
    font-weight: 600;

    @include tablet-landscape {
      font-size: 48px;
    }
  }

  .headers__h1--highlight {
    background: linear-gradient(180deg, rgba(255,255,255,0) 50%, $highlight 50%);
    border-radius: 2px;
    padding: 0 3px;
  }

  .headers__h2 {
    font-size: 22px;
    font-weight: 500;

    @include tablet-landscape {
      font-size: 24px;
    }
  }
</style>