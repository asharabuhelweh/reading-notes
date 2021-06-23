# Routing

## Review, Research, and Discussion

1. ### Do child components have direct access to props/state from the parent?

there is no way to pass props from a child component to a parent component. However, we can always pass around functions from the parent to child component. The child component can then make use of these functions. The function can then update the state in a parent component,

2. ### When a component “wraps” another component, how does the child component’s output get rendered?**

Gets rendered when there is an update to state.

3. ### Can a component, such as `<Content />`, which is a child also be used as a standalone component elsewhere in the application?
They can by rendered using the props.children and the they will be rendered inside the `<Main/>` component.

3. ### What trick can a parent use to share all props with it’s children
 The parent can pass them directly to all children or pass a function to them to share all the states and props.


## Vocabulary

- **props.children**: property allows you to create a generic template component that can be modified by the parent when it is invoked. This means that a parent component can pass whatever is needed in the child component, even generated layout features that can then be rendered by the child.
  
- **Composition**: is a development pattern based on React's original component model where we build components from other components using explicit defined props or the implicit children prop


## React Routing
React Routing is a package you need to install to use it

* React Router has been broken into three packages: react-router, react-router-dom, and react-router-native.
  
* If we are building a website (something that will be run in browsers), so we will install react-router-dom.


* The `<BrowserRouter>` should be used when you have a server that will handle dynamic requests (knows how to respond to any possible URI), while the `<HashRouter>` should be used for static websites (where the server can only respond to requests for files that it knows about).


* A React Router component that does not have a router as one of its ancestors will fail to work.

Rendering a `<Router>`

- **Router components only expect to receive a single child element.** To work within this limitation, it is useful to create an `<App>` component that renders the rest of your application. Separating your application from the router is also useful for server rendering because you can re-use the <App> on the server while switching the router to a <MemoryRouter>.

* The `<Route>` component is the main building block of React Router. Anywhere that you want to only render content based on the location’s pathname, you should use a `<Route>` element.


The `<App>`
Our application is defined within the `<App>` component. To simplify things, we will split our application into two parts. The `<Header>` component will contain links to navigate throughout the website. The `<Main>` component is where the rest of the content will be rendered.


## What does the \<Route> render?

Routes have three props that can be used to define what should be rendered when the route’s path matches. Only one should be provided to a \<Route> element.

1. component — A React component. When a route with a component prop matches, the route will return a new element whose type is the provided React component (created using React.createElement).
2. render — A function that returns a React element. It will be called when the path matches. This is similar to component, but is useful for inline rendering and passing extra props to the element.
3. children — A function that returns a React element. Unlike the prior two props, this will always be rendered, regardless of whether the route’s path matches the current location.

The element rendered by the \<Route> will be passed a number of props. These will be the match object, the current location object 6, and the history object (the one created by our router).

It can be useful to group routes that share a common prefix in the same component. This allows for simpler parent routes and gives us a place to render content that is common across all routes with the same prefix.

## Path names

A `<Route>` expects a path prop, which is a string that describes the pathname that the route matches — for example, `<Route path='/roster'/>` should match a pathname that begins with /roster. When the current location’s pathname is matched by the path, the route will render a React element. When the path does not match, the route will not render anything.

When it comes to matching routes, React Router only cares about the pathname of a locatio

## Routers Organiztion

`<Route>`s can be created anywhere inside of the router, but often it makes sense to render them in the same place. You can use the `<Switch>` component to group `<Route>`. The `<Switch>` will iterate over its children elements (the routes) and only render the first one that matches the current pathname.

In order to match a path in our application, all that we have to do is create a `<Route>` element with the path prop we want to match.



## Path params

Sometimes there are variables within a pathname that we want to capture. For example, with our player profile route, we want to capture the player’s number. We can do this by adding path params to our route’s path string.

## Links

To navigate between pages, if we were to create links using anchor elements, clicking on them would cause the whole page to reload. React Router provides a \<Link> component to prevent that from happening. When clicking a \<Link>, the URL will be updated and the rendered content will change without reloading the page.

\<Link>s use the to prop to describe the location that they should navigate to. This can either be a string or a location object (containing a combination of pathname, search, hash, and state properties). When it is a string, it will be converted to a location object.


### Hooks
React Router ships with a few hooks that let you access the state of the router and perform navigation from inside your components.

- useHistory
  
     The useHistory hook gives you access to the history instance that you may use to navigate.

- useLocation
  
  The useLocation hook returns the location object that represents the current URL. You can think about it like a useState that returns a new location whenever the URL changes.


- useParams
  useParams returns an object of key/value pairs of URL parameters. Use it to access match.params of the current `<Route>`.


- useRouteMatch
  The useRouteMatch hook attempts to match the current URL in the same way that a `<Route>` would. It’s mostly useful for getting access to the match data without actually rendering a `<Route>`.