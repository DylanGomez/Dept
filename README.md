# dept-assignment

This application has been built to test my level of skill in the application process of a vacancy put out by DEPT.
The assesment was to build a website based on assets provided by DEPT. The URL for the assesment can be found here: url

For this project I've decided to use the Vue framework accompanied with the Vuetify UI library. I chose Vue since I have the most experience with building fast and easily explainable applications. Adding Vuetify to the project removes the hassle of building small components like cards, styled lists and expandable content transistions. (Let's be honest, I wouldn't be a programmer if I didn't take at least some shortcuts ;) )

I tried to keep the app as responsive as possible, I added some extra media queries to make the application as mobile friendly as possible.

In total I've worked around 5-6 hours in my free time to get to the current state of the application.

# What has been build and why

For this assesment I focused on building different reusable components where one of the goals was to make small, readable components which can be easily rebuilt to fit different purposes.

The CaseBlock component uses different props which makes it possible to build a 4 column grid structure without needing to adjust any code. Cases can simply be added by changing the cases.json file. Which in theory could be retrieved by an API action and saved in the store. Which could make so that the data can be easily filtered either server or client side.

Of course, a linter has been used (see eslintrc.js for the exact rules) and other coding best practices have been used.

# What has not been build and why

Since I set myself on a time limit since I can get pretty perfectionistic about these kind of assignments I had to stop myself from building too much.

- Filtering
- The contact form
- Footer

I didn't get to build these assets since I focused more on the reusable components, and it all honesty, I was a bit too focused to get the grid system in the CaseBlock component to line out right (and I'm still not completely satisfied with it).

If you need to see some more of how I code, I have just added a repository of a small test project where I used JSON-Server in combination with the VueX store.

If there are any questions whatsoever, feel free to contact me.

## Project setup

```
yarn install
```

### Compiles and hot-reloads for development

```
yarn serve
```

### Compiles and minifies for production

```
yarn build
```

### Lints and fixes files

```
yarn lint
```
