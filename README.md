# Client(Alternatively Src) #
Is the Root directory and contains; app.html, app.js and main.js

# Components (Alternatively templates) #



Components are where shared components exist. 

**Generally you have two types of components**

**Application specific** -- such as the main components folder which contains nav-bar, header, custom-table.  Each of these can stand alone or be made up of custom elements or other components. These are non-route specific components. 

**Route specific** -- Where the route has its own component folder.  Such as the route-with-componets route where I want to make sure I have an edit-component as well as a details-component, as well as any other components that make up the main component. This is so anywhere I am showing the main route component I can use the details view and anytime I need to make an edit, the component is ready to rock.

#Models#
These are the classes that define the various models in your application, at each level. At the root level we have application-wide models such as the User.

# Resources #
The resources directory is where any global resources for your applications should be placed. The index.js file allows this directory to act as an Aurelia feature that is installed in main.js

# Routes #
The routes directory is a great way of grouping content. Typically if a route implements a child router all of it's content and files relevant only to that child route go nested inside to keep things clean.

**Routes themselves can be made up of it's own components, models, and routes(sub routes)**. 

**The route-with-componets**, using a face as the main component is made up of left-eye, mouth, right-eye etc..., these components are used to build the face. In keeping it modular you can do things like changing how the right eye works by changing the right eye component without affecting the rest of what makes up the face. 


**The route-with-componets-models-subroutines **shows a combination of components, modules, and routes.

**Index.js and Index.html is the entry point**, but I am not sure if I want to use the index style or just have the face.js and face.html as the entry point 

# Services #
In the Services directory goes all of your JavaScript which performs a service for other files such as your view-models. These are usually services for things like fetching data and returning it in a standard format.

# Lib #
Where generic non-app specific code lives. Utility classes and functions for doing utility-like tasks

# Assets #
Where all assets of the app live (with separate sub-folders)

# Models #


# Maybe fore electron only #

> Two Package.json files

One is in the root and contains all of you dev dependencies.
The other is in your client or src folder and contains runtime
dependencies.

The reason is that you do not want to package all of your development
dependencies with your runtime.
