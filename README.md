## VueJS forms and Virtual DOM Playground

A little WYSIWYG Vue SPA to take and plug into your back-end of choice 🚀 
In my case REST and PHP, vanilla PHP to keep it simple. Also works with
Laravel or CI3+ as you would expect. 

**🙃 git with it or git lost jk lol #gitFlow **


## Getting Going with Vue CLI

You need to have npm to install vue, google is your friend. SPA will
live inside repos ./tasks folder you can cd there and run "npm run serve".

1. vue create tasks
    Run this command in terminal for the cli to start your boiler plate
2. Manual install
    In this menu with arrows and space you can select features you need
    like PWA support for instance, hit enter when done to for next menu.
3. Vue 3.x 
    In the next menu you need to pick a vue version, you can feature
    proof if you build with version 3.
4. Decicated Config Files
    In the next menu select that you want your config to be saved localy.
5. Dont save preset
    This step is optional in final menu but i suggest you dont create the 
    preset to select manualy again next time. 
6. cd tasts
    You are now ready to cd into your new Vue app.
7. npm run serve
    To get localhost going type/run this command in the terminal. This
    should launch and open it in your browser

## Making Components with Vue

Vue makes it easy to make a component and its structure is also easy to follow. What makes it unique is that the template style and script live inside the vue file. You can think of this like a controller where you can write or link CSS, template and script files. 

1. Step one make a new file with the name of your new component and a 
vue extention in the components folder. 
    Header.vue lives in ./tracker/src/components/Header.vue
2. You must then import this new component in your App.vue file
    import Header from './components/Header.vue'
3. Also you will need to register this component for vue to access it
    export default {
        name: 'App',
        components: {
            Header
        }
    }
4. You can now use your component as expected in your view calling your
new components tagname 
    <Header / >

## Authors

👤 **Miguel Angel Enciso Sanchez**

- Github: [@rootDEV2990](https://github.com/rootDEV2990)
- Twitter: [@m29902](https://twitter.com/m29902)
- Linkedin: [linkedin](https://www.linkedin.com/in/miguel-enciso-6474741a1/)
- Medium: [medium](https://medium.com/@website.dev)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!

Feel free to check the [issues page](issues/).

## Show your support

Give a ⭐️ if you like this project!

Bitcoin donations accepted ;)

1AD5ANtHmqemTZ2Qmv5UqJAMijTNyCAH8D 🚀
