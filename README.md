# CAPETA

This repository contains the files from the site of brazillian think tank CAPETA - Capital e Estado, a research/activist group about Capital and State.

CAPETA - Capital and State, is a group of research, extension and political activism in favor of the socio-economic-political-cultural development of nations on the periphery of global capitalism. We are professors and students of economics, international relations, and the humanities whose starting point is a renewed Political Economy, in which the material and the social go together. For us, market and state, money and power, are social institutions constituting each other. In particular, the State can and should be treated as a category of analysis endogenous to the functioning of capitalism; which means that the dynamics of power are complementary to those of capital accumulation. 

The central research of the group at the moment (2018) consists of a series of studies on the loss of sovereignty of peripheral nations in carrying out developmental policies due to the current global financial (in) order based on the supremacy of the dollar, on the free mobility of capitals, and the communicational power of the global elite in the construction of “secret” information systems. This research is constructed via readings in a large group, scriptures by many hands, and submission of all production to the group's criticism and to public opinion in general before and as a priority rather than to academic hosts and specialized magazines, which does not imply excluding them. 

It is not about political activism, our main objective is to contribute to the articulation of groups of thinkers and activists of the most diverse common policies, provided that they see in the monetary and financial system in force at the international level a structural limitation to national economic development. viable, socially just and ecologically sustainable. Thus, our greatest willingness is to collaborate in the construction of a discussion network capable of thinking, formulating and proposing policies that are more consistent with these objectives. 

For that, it is necessary, in academic terms, to overcome the analyzes still stuck in purely abstract models, trying to bring us closer to methods that involve an analysis and the treatment of data with the aim of providing greater empirical basis to our propositions. In political terms, it is urgent to overcome the merely academic discussion.

[Site Hosted Here](https://capeta.info/)

This source code is derived from https://github.com/Thomashighbaugh/coolStarter.

---

# TECHNOLOGY

We propose...

## Set Up
In order to manipulate the site's cms features the following steps are required to produce the development server and run it locally. 

- Install Node.js for your platform (Node Version Manager (nvm) is highly recommended) 
- open a terminal/command line
- navigate to this folder/directory
- run `npm i -g yarn`
- run `yarn install`
- run `yarn develop`
- open browser to http://localhost:8000

### Source Code 

#### Javascript Version // Library
The site utilizes and conforms to the conventions of the React library/framework which is a library enabling the construction of Javascript as a series of components, isolating various logical aspects of the application in a modular format. The files written in this Javascript variant are across the `src` folder.

In combination with React, a lot of the logic that is utilized within this site is derived from Node.js and is wrapped in React components, or site configuration files, determining which is clearly node vs. node+configuration is hard to do, as they are isolated into functional portions due to the React development pattern, otherwise I would 
specify an example. 

In order to be readable by client machines, which React is not, it is *transpiled* into Javascript by Babel. This also makes the source code compliant with older browsers, turning ES6 & ES7 into vanilla JS. 


#### Static Site Generator
This site is additionally processed by an application called Gatsby.js which takes the components and JSON files within `content/pages` and renders them into HTML5 and CSS3. This means that the server is just caching a series of HTML and CSS files that user's request, saving hardware resources and making it so that the developer may add a content manager for writers to add content without need to edit source code. 

As input, template files create content blocks, which then are called by the `content/pages` files and these are all wrapped within configurations provided in `src/components/pageLayout` and `src/components/siteLayout` that includes the React Helmet package enabling the modification of the generated head element in the generated html that enables SEO in the generated site, an otherwise impossible task. 



Configuration is provided in the files `gatsby-config.js`, `gatsby-browser.js` and `gatsby-node.js` which include a list of additional plugins added to the SSG to extend its functionality, such as reading the Markdown files, adding in images, etc. 

#### Markdown 
The articles are written in Markdown, a quick markup that utilizes HTML
elements ergonomically. They are taken as input by the SSG to dynamically produce pages for each in the generated code. 

### CMS

The Content Management System that is being utilized by this site is self hosted, based at [TinaCMS](http://tina.io). This site do not depends on a database, all content modifications are sent to markdown files versioned at a git repository.

#### Features

- Live Editing Content
    - Editing Tabs on Articles Content 

- Page and Site Editing 
    - Theme Editing 
    - Modifications of the Site's General Configuration
   



