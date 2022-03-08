# dept-assignment

This application has been built to test my level of skill in the application process of a vacancy put out by DEPT.
The assesment was to build a website based on assets provided by DEPT. The URL for the assesment can be found here:

For this project I've decided to use the Vue framework accompanied with the Vuetify UI library. I chose Vue since I have the most experience with building fast and easily explainable applications. Adding Vuetify to the project removes the hassle of building small components like cards, styled lists and expandable content transistions. (Let's be honest, I wouldn't be a programmer if I didn't take at least some shortcuts ;) )

In total I've worked around 5-6 hours in my free time to get to the current state of the application.

# What has been build and why

For this assesment I focused on building different reusable components where one of the goals was to make small, readable components which can be easily rebuilt to fit different purposes.

The CaseBlock component uses different props which makes it possible to build a 4 column grid structure without needing to adjust any code. Cases can simply be added by changing the cases.json file. Which in theory could be retrieved by an API action and saved in the store. Which could make so that the data can be easily filtered either server or client side.

# What has not been build and why

Let me come back on this one tomorrow :)

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
