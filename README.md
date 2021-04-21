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

## Component Props

1. You can define your own props to update values in component with
the new components html tag
    <Header title='Tasks'>
2. Update your component file ./tracker/src/components/Header.vue to 
recive the new string. under the name of the exported component add the props: and coresponding name in our case title with a type of string
    export default {
        name: 'Header',
        props: {
            title: {
                type: String,
            }
        }
    } 
3. You may now call use this in your template calling the expression 
inside our html with {{ }}
    <template>
        <header>
            <h1>{{title}}</h1>
        </header>
    </template>

## Calling Functions with Vue

1. Add the on click like you would with JS. In your component file 
Button.vue for example you can call the fuction with vue in your html
    <button @click="addTask()"><button>
2. Update your script to register the fuction and write your code
    methods: {
        addTask() {
            alert('Function good to go! Your code block can go here..')
        }
    }

## Passing Arrays as Props in Vue

1. Inside your html components tag we pass the tasks array to 
tasks prop inside the Tasks Component.
    <Tasks :tasks="tasks">
2. You need to update your component file to take in an array of data
as a prop in your components html tag. ./tracker/src/components/Tasks.vue
    props: {
        tasks: Array,
    }
3. Then dont forget to update your ./tracker/src/App.vue file importing 
your tasks component
    import Tasks from './components/Tasks'
4. Lastly reginster the component so vue can identify its name.
    export default {
        name: 'App',
        components: {
            Header,
            Tasks
    }
5. I have added test data in ./tasks/src/App.vue for you to use as a test
array this can also be modified to pull in http json if you need it
    data() {
        return {
        tasks: []
        }
    },
    //populates tasks: []
    created() {
        //this can also contain json return via GET HTTP
        this.tasks = [
            {
            id: 1,
            text: 'Doctors Appointment',
            day: 'March 1st at 2:30pm',
            reminder: true,
            },
            {
                id: 2,
                text: 'Meeting at School',
                day: 'March 3rd at 1:30pm',
                reminder: true,
            },
            {
                id: 3,
                text: 'Shopping for Food',
                day: 'March 3rd at 11:30am',
                reminder: false,
            }
        ]
    }

## Looping Through Arrays 
1. To loop and display your arrays data in your views 
you can use the v-for directive. Update the component file 
./tracker/src/components/Tasks.vue to display your array 
data in the <template v-for="x in array"> tag here you define a 
temp var name like x to use in the loop
    <div v-for="task in tasks">
        
    </div>
2. We must also provide a unique key like with react for this we will use 
the id
    <div :key="task.id" v-for="task in tasks">
    </div>
3. Finaly to access values from each object in our array we will use expressions inside of double braces {{ }}
    <div :key="task.id" v-for="task in tasks">
        <h3>{{ task.text }}</h3>
    </div>



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
