# cbr-modern

## Reflection 

This assignment required me to use an API and client-side framework in order to create a web application for the organisation, Canberra Modern. The development process began by consulting the Canberra Modern design brief, which gave insight into their mission, general info, website needs, visual identity and audience. After familiarising myself with the organisation’s identity, I created a series of sketches, outlining the general layout of the website. A priority during this iteration process was making the site easy to navigate, whilst maintaining an original and engaging design.  
Upon choosing the client-side framework, I opted for Vue.JS and Nuxt.JS. These frameworks are considered fairly intuitive for beginners and have a large online community. They were further recommended as the majority of the class was also planning to use Vue and Nuxt.JS, meaning there would be further opportunity for collaboration and receiving aid from the tutor.  

The initial coding phase presented challenges, as the frameworks appear very overwhelming when opened in Visual Studio Code. Fortunately, the class was provided with a GitHub file that would help indicate which files must be edited and which should be left alone. 

I immediately had problems however, as I was unable to view the website online, despite following the steps available in the markdown file. This was ultimately resolved, as I simply had to download Yarn according to a specific Windows procedure.

After overcoming this issue in class, I began actually coding and editing the site. Using the available BuildingsList.vue and pages/buildings/index.vue for reference, I tried to understand how to call an API and integrate it into the website. Using the API links available in Modules, I was then able to re-apply the steps on an EventsList.vue page. These steps affirmed that I was on the right track, and could successfully fetch data in an array. 
My next goals involved separating the Events to be arranged by year and providing an About page. After receiving some advice from my classmate, I created an Events folder for each year, with a corresponding index, slug and components page. These could then be used to repeat the previous steps, as well as a specific Navigation bar for traversing the separate years. Unfortunately, I couldn’t figure out how to remove the occasional letter jargon (i.e. ‘&M0*%’) that appears in some of the event titles. 

For the About page, I initially tried adapting the previous method of the BuildingsList.vue in order to fetch About data, however, this was unsuccessful. I then realised that the v-html directive could make a variable to render content. I proceeded to apply this technique on the Homepage, as it also lacked content. As the Homepage did not have an API to reference on the Canvas Modules page, I realised I could simply use the ‘All Pages’ link and add the slug in order to isolate a specific page. 

During the design stage, I employed CSS to style the website. I chose to directly pick colours from the logo, in order to maintain consistency with the organisation’s brand identity. I additionally opted for minimal styling, in order make navigation easier. However, I added hover effects to communicate responsiveness to the user. I changed the favicon to the Canberra Modern logo, as the Vue logo was not fitting for the site. I drew inspiration from the WordPress version of the website, opting for sans serif fonts, for legibility and a more formal appearance.  

This project has been a great learning opportunity as well as collaborating with one another. I’ve gained a significant insight into operating frameworks and calling APIs using arrays. 

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## Special Directories

You can create the following extra directories, some of which have special behaviors. Only `pages` is required; you can delete them if you don't want to use their functionality.

### `assets`

The assets directory contains your uncompiled assets such as Stylus or Sass files, images, or fonts.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/assets).

### `components`

The components directory contains your Vue.js components. Components make up the different parts of your page and can be reused and imported into your pages, layouts and even other components.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/components).

### `layouts`

Layouts are a great help when you want to change the look and feel of your Nuxt app, whether you want to include a sidebar or have distinct layouts for mobile and desktop.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/layouts).

### `pages`

This directory contains your application views and routes. Nuxt will read all the `*.vue` files inside this directory and setup Vue Router automatically.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/get-started/routing).

### `plugins`

The plugins directory contains JavaScript plugins that you want to run before instantiating the root Vue.js Application. This is the place to add Vue plugins and to inject functions or constants. Every time you need to use `Vue.use()`, you should create a file in `plugins/` and add its path to plugins in `nuxt.config.js`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/plugins).

### `static`

This directory contains your static files. Each file inside this directory is mapped to `/`.

Example: `/static/robots.txt` is mapped as `/robots.txt`.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/static).

### `store`

This directory contains your Vuex store files. Creating a file in this directory automatically activates Vuex.

More information about the usage of this directory in [the documentation](https://nuxtjs.org/docs/2.x/directory-structure/store).

## Node version

nvm install v16.15.0

