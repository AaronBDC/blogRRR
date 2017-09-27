Section 9 - React Router and Redux Form

Section: 90 / 37React Router + Redux Form115. Important Note0:00
Important NoteSection 9, Lecture 115The following section contains updated content that uses React Router v4 and Redux Form v6.  I recommend you watch these videos, and skip the previous section on React Router + Redux Form!



116. App Overview and Goals6:49117. Posts API9:20

https://reduxblog.herokuapp.com

118. Quick Note0:00
Quick NoteSection 9, Lecture 118Oops!  Mistake on my part ahead!  In the next video, I tell you to run the command npm install --save react-router@4.0.0 .The React Router project has now been broken up into a couple of different libraries.  The correct command to run is npm install --save react-router-dom@4.0.0 <--run this instead.  This library contains the flavor of react-router related to working with the DOM, as opposed to other platforms (like React Native).

A119. Installing React Router3:00

the url 

react-router install it anddiscuss what it does

npm i --save react-router-dom@4.0.0 

120. What React Router Does5:36
- how the web used to work (early 1990's and 2010's)
- user is changing the url inside their browser.


121. The Basics of React Router8:58

- in atom, open src folder index.js
- add BrowserRouter, Route , from 'react-router-dom';
- the route component is the real workhourse of all things react-router
- this object Route is a react component we can render inside any other react component we put together inside of our application.
- the purpose of the route component is to provide that configuration that 
- will say "hey if the URL looks like this then i want to show this component."
- the route object/route component is all about providing some customization or configuration to react router.
  
- old ERROR:
bundle.js:86 Uncaught TypeError: Super expression must either be null or a function, not undefined
    at _inherits (bundle.js:86)
    at bundle.js:91
    at Object.<anonymous> (bundle.js:111)
    at __webpack_require__ (bundle.js:20)
    at Object.<anonymous> (bundle.js:47)
    at __webpack_require__ (bundle.js:20)
    at bundle.js:40
    at bundle.js:43
_inherits @ bundle.js:86
(anonymous) @ bundle.js:91
(anonymous) @ bundle.js:111
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43
util.js:228 Google Maps API warning: NoApiKeys https://developers.google.com/maps/documentation/javascript/error-messages#no-api-keys
RB.j @ util.js:228
(anonymous) @ js:140
(anonymous) @ js:63
(anonymous) @ js:61
(anonymous) @ js:63
(anonymous) @ js:116
(anonymous) @ js:61
(anonymous) @ js:116
ge @ js:63
fe.na @ js:116
(anonymous) @ stats.js:1

- after updating a typo in lodash on the posts_index component
- it compiles but an error @ Add New
- success screenshot at 0713 - sept 26 2017 - @ genie.local desktop

- errors app and at Add a post button

- Warning: Failed propType: Invalid prop `component` of type `object` supplied to `Route`, expected `function`.
warning @ bundle.js:2315
checkPropTypes @ bundle.js:19554
validatePropTypes @ bundle.js:19573
createElement @ bundle.js:19607
(anonymous) @ bundle.js:102
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43

bundle.js:50575 GET http://reduxblog/herokuapp.com/api/posts?key=dasriderclip1234 net::ERR_NAME_NOT_RESOLVED
dispatchXhrRequest @ bundle.js:50575
xhrAdapter @ bundle.js:50409
dispatchRequest @ bundle.js:51069
Promise resolved (async)
request @ bundle.js:50246
Axios.(anonymous function) @ bundle.js:50256
wrap @ bundle.js:50153
fetchPosts @ bundle.js:49625
(anonymous) @ bundle.js:21186
componentDidMount @ bundle.js:49679
notifyAll @ bundle.js:6553
close @ bundle.js:16311
closeAll @ bundle.js:6914
perform @ bundle.js:6861
batchedMountComponentIntoNode @ bundle.js:2761
perform @ bundle.js:6848
batchedUpdates @ bundle.js:10885
batchedUpdates @ bundle.js:6353
_renderNewRootComponent @ bundle.js:2955
ReactMount__renderNewRootComponent @ bundle.js:1549
_renderSubtreeIntoContainer @ bundle.js:3029
render @ bundle.js:3049
React_render @ bundle.js:1549
(anonymous) @ bundle.js:90
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43

util.js:228 Google Maps API warning: NoApiKeys https://developers.google.com/maps/documentation/javascript/error-messages#no-api-keys
UB.j @ util.js:228
(anonymous) @ js:140
(anonymous) @ js:63
(anonymous) @ js:61
(anonymous) @ js:63
(anonymous) @ js:116
(anonymous) @ js:61
(anonymous) @ js:116
(anonymous) @ js:61
(anonymous) @ js:116
fe @ js:63
ee.na @ js:116
(anonymous) @ util.js:1


ERRORS AT ADD A NEW POST (Localhost:8080/posts/new):

bundle.js:2315 Warning: Failed propType: Invalid prop `component` of type `object` supplied to `Route`, expected `function`.
warning @ bundle.js:2315
checkPropTypes @ bundle.js:19554
validatePropTypes @ bundle.js:19573
createElement @ bundle.js:19607
(anonymous) @ bundle.js:102
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43

bundle.js:2315 Warning: React.createElement: type should not be null, undefined, boolean, or number. It should be a string (for DOM elements) or a ReactClass (for composite components). Check the render method of `Route`.
warning @ bundle.js:2315
createElement @ bundle.js:19586
render @ bundle.js:24713
_renderValidatedComponentWithoutOwnerOrContext @ bundle.js:7798
_renderValidatedComponent @ bundle.js:7818
ReactCompositeComponent__renderValidatedComponent @ bundle.js:1549
mountComponent @ bundle.js:7431
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountChildren @ bundle.js:14311
_createContentMarkup @ bundle.js:11486
mountComponent @ bundle.js:11374
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponentIntoNode @ bundle.js:2745
perform @ bundle.js:6848
batchedMountComponentIntoNode @ bundle.js:2761
perform @ bundle.js:6848
batchedUpdates @ bundle.js:10885
batchedUpdates @ bundle.js:6353
_renderNewRootComponent @ bundle.js:2955
ReactMount__renderNewRootComponent @ bundle.js:1549
_renderSubtreeIntoContainer @ bundle.js:3029
render @ bundle.js:3049
React_render @ bundle.js:1549
(anonymous) @ bundle.js:90
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43

bundle.js:1231 Uncaught Error: Element type is invalid: expected a string (for built-in components) or a class/function (for composite components) but got: object. Check the render method of `Route`.
    at invariant (bundle.js:1231)
    at ReactCompositeComponentWrapper.instantiateReactComponent [as _instantiateReactComponent] (bundle.js:7157)
    at ReactCompositeComponentWrapper.mountComponent (bundle.js:7434)
    at ReactCompositeComponentWrapper.wrapper [as mountComponent] (bundle.js:1549)
    at Object.mountComponent (bundle.js:5741)
    at ReactCompositeComponentWrapper.mountComponent (bundle.js:7436)
    at ReactCompositeComponentWrapper.wrapper [as mountComponent] (bundle.js:1549)
    at Object.mountComponent (bundle.js:5741)
    at ReactDOMComponent.mountChildren (bundle.js:14311)
    at ReactDOMComponent._createContentMarkup (bundle.js:11486)
invariant @ bundle.js:1231
instantiateReactComponent @ bundle.js:7157
mountComponent @ bundle.js:7434
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountChildren @ bundle.js:14311
_createContentMarkup @ bundle.js:11486
mountComponent @ bundle.js:11374
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1549
mountComponent @ bundle.js:5741
mountComponentIntoNode @ bundle.js:2745
perform @ bundle.js:6848
batchedMountComponentIntoNode @ bundle.js:2761
perform @ bundle.js:6848
batchedUpdates @ bundle.js:10885
batchedUpdates @ bundle.js:6353
_renderNewRootComponent @ bundle.js:2955
ReactMount__renderNewRootComponent @ bundle.js:1549
_renderSubtreeIntoContainer @ bundle.js:3029
render @ bundle.js:3049
React_render @ bundle.js:1549
(anonymous) @ bundle.js:90
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43

util.js:228 Google Maps API warning: NoApiKeys https://developers.google.com/maps/documentation/javascript/error-messages#no-api-keys
UB.j @ util.js:228
(anonymous) @ js:140
(anonymous) @ js:63
(anonymous) @ js:61
(anonymous) @ js:63
(anonymous) @ js:116
(anonymous) @ js:61
(anonymous) @ js:116
(anonymous) @ js:61
(anonymous) @ js:116
fe @ js:63
ee.na @ js:116
(anonymous) @ util.js:1


- now we've imported these objects and we've created our two components lets wire them all up.
- create new instances of route
- pass path and compnent
- path is always a string that says if a user goes to this route i want to show this component
- if things dont match up then dont
- else do nothing
-success screens at 727

-- so essentially we use that route component to just show or hide a child component depending on the URL
-- success screenshots taken at genie local desktop at 731


122. Route Design6:31

-- name doesnt have to match for compnent and path names

route:/
component: {PostsIndex}
-- main route is the slash or root /

Route: /posts/* (wildcard)
component: PostsShow
--- might look like this:
  <Route path="/posts/:id" component={PostsShow} />
-- colon tells router to be kind of a fuzzy match or a kind of a wildcard
-- so if a user tries to goto post/1 or post/1 or post/3 whatever it might be,
  react router is going to consider that /1 or /2 to be a wildcard and its going to try to 
  greedily match that route against this component right here.
  -- PostsShow component is going to be responsible for fetching a very particular post and showing it on the screen.
   
Route: /posts/new
Component: PostsNew
-- the last route is all about showing or not showing a component to the user that they can use to create brand new post.
--route something like /posts/new


123. Our First Route Definition5:57
-- commit made on master branch

-- new posts_index component

-- noticed existing app component

-- from index.js in src. remove hello and goodbye test components.

-- from index.js in src. remove the routes in the render method for the header text, hello and goodbye routes

-- now that we have react router, we dont need app component

-- delete import statement and the appjs component file

-- import PostIndex from compnents/posts_)index
import PostsIndex from './components/posts_index';

-- associate posts_index compnent to route root path /
          <Route path="/" component={PostsIndex} />

-- REMEMBER: THE WAY I"M LEARNING THIS INTRODUCES A BUG WITH REACT ROUTER @COMEBACK EXPLAIN
-- the bug is left in because he gaurantees we will run into it ourselves in production for our own projects when we use react router for the first time.
-- its a very common mistake that everyone runs into when first using react-router
-- we will fix it (hint its one word we add to this prop in index?)
-- test in browser

-- 
124. State as an Object9:07

-- move over to redux side of things for wiring it up
-- different design for state object this time.
-- look at api for posts
-- we get array of posts, 
-- each post has an id
-- how we are different for structure
-- interaction between react router and redux
-- stuff gets crazy here
-- app state and url 
-- url is a critical piece of state.
-- whenever state changes, we rerender
-- current route is a piece of state inside of our
-- id for that route is really provided by actvePost key
-- we dont need activePost state so we get rid of it because dont need it inisde the URL

-- so in other words whenever we render the post show component,
we can look at the URL,
we can look at our list of posts,
and we can say "hey find the post with tthe id 5 out of this list and show it on the screen to the user"

-- thats step 1 in changing our state structure here.
-- step 1 is to understand why we really dont need that active post piece of state.
-- thats reasonable because the URL does reflect the ID so we really dont need this exrtra extra piece of state in here because we can manually calculate it by looking at our posts list and the URL the a user is looking at at any given time.
-- screenshot takein around 0804 at bam

-- next change - use object instead of array
--if we used an array we'd have to use a find or a loop for the array to find the post
-- going from posts in array to posts in object makes it a little bit eaiser to use and involves less code:
  state.posts[postId]
-- the postId above is assuming we pulled the URL and made it into the postId variable
-- the idea is called an object for holding properties or records inside of redux is a very advanced concept.
-- so this really is a challenging refactor right here that im suggesting but I got to tell you this is how we really do it in production.
-- this is how we really build large applications that scale well.
-- it is a little bit painful refactor as we go through this but you know its definitely something we have to do out of neccessitty.

 B125. Back to Redux - Index Action7:07

-- action creator to fetch a list of posts
-- and somehow turn the array of posts that we get back from our API into this object that contain the posts as well.

-- install axios and redux promise

-- rewire redux promise as a middleware

-- import promise ]redux promise

-- pass into applymiddleware call

-- import axios library into src actions index.

-- I UPDATED INDEX.JS IN SRC/ACTIONS TO REFLECT A BETTER ROOT_URL
FROM :
  const ROOT_URL = 'http://reduxblog/herokuapp.com/api';

TO: 
  const ROOT_URL = 'http://reduxblog/herokuapp.com/api/posts';
TO:
  const ROOT_URL = 'http://reduxblog.herokuapp.com/api';

-- UDPDATED API_KEY
 const API_KEY = '?key=DASRIDERCLIP1234';


-- FORMED REQUEST:
  const request = axios.get(`${ROOT_URL}/posts${API_KEY}`);

-- ADD IT TO THE PAYLOAD OF THE ACTION WE'RE RETURNING:

  ///action object
  return{
    type: FETCH_POSTS,
    payload: request
  };

-- WE'RE MAKING THE AXIOS GET REQUEST,
THEN WE'RE ASSIGNING THE REQUEST TO THAT PAYLOAD PROPERTY OF THE ACTION 
THAT WE'RE RETURNING.
-- BECAUSE THE REQUEST IS BEING ASSIGNED TO THE PAYLOAD PROPERTY, THE REDUX PROMISE MIDDLEWARE THAT WE MADE USE OF WILL AUTOMATICALLY RESOLVE THIS REQUEST
FOR US WHENEVER IT SEES THIS ACTION COME ACROSS.
-- SO BY THE TIME THIS ACTION ARRIVES IN THE REDUCER, THE PAYLOAD PROPERTY WILL
CONTAIN THE RESPONSE OBJECT FROM AXIOS 
WHICH WILL HAVE OUR BIG OLD ARRAY OF POSTS.


126. Implementing Posts Reducer10:29
-- when testing this out, an empty array might come back because we are testing
-- we dont have any post stored in the api so it will come back empty
-- if we made this request now an empty array would come back (expected result)
-- once we start to add in the functionality to add a new post to our API well then things are going to be a little bit more lively inside our application.
-- lets work on the redux side of things now
-- the reducer which is going to store or produce the post piece of state

test code:
`````

start


``

const posts = [
  { id: 4, title: "hi"},
  { id: 25, title: "bye"},
  { id: 36, title: "hows it going"}
 ];

const state = _.mapKeys(posts, 'id' )

state["4"]


```

output
````

{"id":4,"title":"hi"}

```

actual code:

      return _.mapKeys(action.payload.data, 'id');

127. Action Creator Shortcuts8:06

-- in lifecycle method, its an ideal location to kick off our data loading process..
//lifecycle method
    //automatically called when this component has shown up in the dom.
    //when we call our api as soon as the component is about to be shown
    //perfect for something one time like loading...
    this.props.fetchPosts();
    
-- retest and examine network tab of dev console /inspector

-- screenshot of succes stkaen at 926 at genie .local desktop

 
128. Rendering a List of Posts9:19
--connect mapStateToProps whenever we want to consume the data from an API

 FROM:
 
   export default connect(null, { fetchPosts })( PostsIndex );

TO:
  export default connect(mapStateToProps, { fetchPosts })( PostsIndex );

screenshots taken at 953 at genie local

-- two console logs 
-- everything renders one time without any posts
-- component rerenders after fetch post is populating

-- notice the key of the id

-- put together a helper funciton inside the 
  render(){
    console.log(this.props.posts);
    return(
      <div>
        <div className="text-xs-right">
          <Link className="btn btn-primary" to="/posts/new">
            Add a post
          </Link>
        </div>
        <h3> Posts </h3>
      <ul className="list-group">
        {this.renderPosts()}
      </ul>
     </div>
    );
  }
  
-- 

129. Creating New Posts5:42
-- I cant see the posts rendered but I can see them logged in the console
-- screenshot of failure at 958 on genie local deskotp

-- Warning: Failed propType: Invalid prop `component` of type `object` supplied to `Route`, expected `function`.
warning @ bundle.js:2315
checkPropTypes @ bundle.js:19554
validatePropTypes @ bundle.js:19573
createElement @ bundle.js:19607
(anonymous) @ bundle.js:102
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43

--bundle.js:51217 Uncaught (in promise) ReferenceError: post is not defined
    at bundle.js:51217
    at bundle.js:39521
    at bundle.js:40319
    at baseForOwn (bundle.js:39292)
    at bundle.js:40289
    at baseMap (bundle.js:39520)
    at Function.map (bundle.js:43956)
    at PostsIndex.renderPosts (bundle.js:51214)
    at PostsIndex.render (bundle.js:51246)
    at ReactCompositeComponentWrapper._renderValidatedComponentWithoutOwnerOrContext (bundle.js:7798)
(anonymous) @ bundle.js:51217
(anonymous) @ bundle.js:39521
(anonymous) @ bundle.js:40319
baseForOwn @ bundle.js:39292
(anonymous) @ bundle.js:40289
baseMap @ bundle.js:39520
map @ bundle.js:43956
renderPosts @ bundle.js:51214
render @ bundle.js:51246
_renderValidatedComponentWithoutOwnerOrContext @ bundle.js:7798
_renderValidatedComponent @ bundle.js:7818
ReactCompositeComponent__renderValidatedComponent @ bundle.js:1549
_updateRenderedComponent @ bundle.js:7771
_performComponentUpdate @ bundle.js:7755
updateComponent @ bundle.js:7684
ReactCompositeComponent_updateComponent @ bundle.js:1549
receiveComponent @ bundle.js:7616
receiveComponent @ bundle.js:5791
_updateRenderedComponent @ bundle.js:7773
_performComponentUpdate @ bundle.js:7755
updateComponent @ bundle.js:7684
ReactCompositeComponent_updateComponent @ bundle.js:1549
performUpdateIfNecessary @ bundle.js:7632
performUpdateIfNecessary @ bundle.js:5806
runBatchedUpdates @ bundle.js:6388
perform @ bundle.js:6848
perform @ bundle.js:6848
perform @ bundle.js:6345
flushBatchedUpdates @ bundle.js:6406
ReactUpdates_flushBatchedUpdates @ bundle.js:1549
closeAll @ bundle.js:6914
perform @ bundle.js:6861
batchedUpdates @ bundle.js:10885
enqueueUpdate @ bundle.js:6435
enqueueUpdate @ bundle.js:6020
enqueueSetState @ bundle.js:6186
ReactComponent.setState @ bundle.js:16043
handleChange @ bundle.js:20171
dispatch @ bundle.js:20546
(anonymous) @ bundle.js:26105
dispatch @ bundle.js:21280
action.payload.then._extends.payload @ bundle.js:26102
Promise resolved (async)
(anonymous) @ bundle.js:26101
(anonymous) @ bundle.js:21186
componentDidMount @ bundle.js:51209
notifyAll @ bundle.js:6553
close @ bundle.js:16311
closeAll @ bundle.js:6914
perform @ bundle.js:6861
batchedMountComponentIntoNode @ bundle.js:2761
perform @ bundle.js:6848
batchedUpdates @ bundle.js:10885
batchedUpdates @ bundle.js:6353
_renderNewRootComponent @ bundle.js:2955
ReactMount__renderNewRootComponent @ bundle.js:1549
_renderSubtreeIntoContainer @ bundle.js:3029
render @ bundle.js:3049
React_render @ bundle.js:1549
(anonymous) @ bundle.js:90
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43

--util.js:228 Google Maps API warning: NoApiKeys https://developers.google.com/maps/documentation/javascript/error-messages#no-api-keys

-- update from posts_index: removed posts from line 12 to post
-- Thank you Daniel!

C130. A React Router Gotcha4:44

-- supposed to be seeing both components rendered on the screen
-- import the switch component from react-router-dom

-- the switch component only renders
-- the switch needs the most detailed route first

ReactDOM.render(
  <Provider store={createStoreWithMiddleware(reducers)}>

    <BrowserRouter>
      <div>
        <Switch>
          <Route path="/posts/new" component={PostsNew} />
          <Route path="/" component={PostsIndex} />

        </Switch>
      </div>

    </BrowserRouter>
  </Provider>
  , document.querySelector('.container'));


-- 


131. Navigation with the Link Component5:58

-- add navigation between index and new

-- open post_index file inside the components directory

-- navigation on classic html documents use anchor tag

--in react-router, we dont use anchor tags anymore

-- we really want to show a new set of componnets

-- we do not want another fetch

-- import Link from react-router dom is very much like anchor tag for links

          <Link className="btn btn-primary" to="/posts/new">
            Add a post
          </Link>
-- insetad of href we use to property
-- whats the difference between link and anchor
-- link has a few events on the link 

132. Redux Form5:33
-- acts like an alias for reducer throughout app:
    import {reducer as formReducer } from 'reedux-form'
-- anywhere else in the file we will refer to formReducer and not reducer from redux-form

133. Setting Up Redux Form9:27

-- screenshot on bam taken at 1056 for flow of redux form
-- redux form handles and changes to any input
-- those boilerplates will be handled

-- pass two callbacks that validate the user input

-- if valid, handle form submittale

-- user is trying to submit, take data and save to backend sever or whatever.

-- make one field component per each piece of state

-- import field and reduxform from redux-form in posts_new..js of componets

-- reduxForm is very similar to the HOC connect component of react-redux

-- reduxForm allows component talk to redux store

-- wire up reduxform attached to postsnew compnent at bottom

-- make string in form property unique


export default reduxForm({
  form: 'PostsNewForm'
})(PostsNew);




134. The Field Component10:49
--           {...field.input}
-- field.input is an object that contains props and 

we dont have to wire these events up manually:
<input 
  onChange={field.input.onChange}
  onFocus={}
  onBlur = {}>
  
-- passes through all the event handlers 

-- make sure input shows itself as a text type input

D135. Generalizing Fields8:54

-- screenshot at 1113 on genie local deskotop

-- instead of renderTagsField and renderTitleField, mash into one

-- success screenshot taken at genie at 1120

-- all on track and on target



136. Validating Forms10:31

** -- shouldnt have used tags but categories instead

--submit form

--validate input
-- to do validation of forms managed by redux form:
-- define this object :
  const errors = {} ;
  -- we inspect our values object
  
-- then if there is anything wrong wth the form 

-- we append some propeties
--- basically put an if statement then add some title to errors and redux form wont submit it
-- can combine like so:

  //validate the inputs from values
  if(!values.title || values.title.length <3){
    errors.title = "Enter a title!";
  }
  
OR do it broken out:

  //validate the inputs from values
  if(values.title.length <3){
    errors.title = 'Title must be at least 3 characters!';
  }
  if(!values.title){
    errors.title = 'Enter a title!';
  }
  
-- you dont have to do validation in a single if statement
-- you can do validation in multiple if statements 
and then customize the title or the error thats shown to the user
inside each of those different if statemnets
--removing length validation:
//  if(values.title.length <3){
//    errors.title = 'Title must be at least 3 characters!';
//  }

-- condense export
FROM:
export default reduxForm({
  validate: validate,
  form: 'PostsNewForm'
})(PostsNew);

TO:
export default reduxForm({
  validate,
  form: 'PostsNewForm'
})(PostsNew);

--whenevr e user presses a key, the validate function will be called

--values contains allt the user input

-- in order to validate these inputs, and then communicate any possible errors back to redux form,
we have to return an object that we create from the validate function.

-- this is part of redux form where he thinks that its a very simple thing but it can be a little challengeing to grasp exactly what we're doing inside the validate function right here [points to function validate(values){}])].

  //console.log(values) -> {title: 'adsf', categories: 'adsf', content: 'asdf'}
-- WHAT We're supposed to do inside this function:
--1)  we're always going to start off by creating an errors object:
      const errors = {} ;
     - const errors is an empty object
      
  --- 2) then we'll do some logic to validate the inputs from the values object.
  
--- 3) at bottom, return the errors object:

  return errors;

-- if we return an empty object from the validate function (which is what were doing now),
  redux-form assumes that there is absolutely nothing wrong with our form.
    //if errors is empty, the form is fine to submit
-- however if that object has properties what so ever, it will fail validation and not submit form at all
  // if errors has any properties, redux form assumes form is invalid

1) define the errors object
2) inspect our values object 
3) and if there is anything wrong with the form we append some properties to that object.

--REMEMBER: FOR US, WE REALLY JUST CARE ABOUT MAKING SURE THAT A USER HAS ENTERED SOME VALID INPUT FOR EACH OF THE DIFFERENT PROPERTIES. (TITLE, CATEGORIES, AND CONTENT.)

-- validate funciton will be called whenever user tries to submit the form
-- 
137. Showing Errors to Users4:30

-- get errors displayed in our form

-- it is our job to make sure these errors get displayed on the screen

-- reference the field object

-- reference field.meta.error:
	{field.meta.error}
-- this {field.meta.error} is automatically added to that field object from our validate function.
-- the properties errors.title, errors.categories, errors.content are not picked at random
-- these are very specific property names that i chose when we specificy a property errors.title
and then return errors from the validate function,
-- when redux form goes to render say this field right here it looks at the name property
that we provided [points to <form> Fields>]
-- it says "if the errors object has a property assigned to it of title, 
im going to call render field right here [ppoints to component = this.renderfield]] and
im going to  pass along whatever error message exists on that as object 
with a power under the property title"
-- the name title in the field is what is connected to the errors.titlte in validate
-- if the form field's name is changed to blogtitle, no longer any communication
from the validate function to theis particular field.
-- the name property in <field > and the property that we use inside that validate function
must be identical for all these errors to show up correctly.
-- so because those two properties were identically named, the field object automaticaly gets this field.meta.error
-- and this error.right here is going to be the exact same string that we assigned inside of the validate function which is enter a title 
-- so if your working on your project and stuffs not showing up or stuff is not working correctly, do make sure you double check all your propetry names


138. Handling Form Submittal9:30

-- working on submital
-- no button
-- show a button inside form component
-- add a button with a type submit and class btn btn-primary
        <button type="submit" className="btn btn-primary">Submit</button>


-- add onSubmit for form:
      <form onSubmit={handleSubmit(this.onSubmit.bind(this))}>
-- doesnt post data to backend
-- we are still resposnbiel take data from form and do something with it
  onSubmit(values){
    console.log(values);
  }
  render(){
    const { handleSubmit } = this.props;

    return(
      <form onSubmit={handleSubmit(this.onSubmit.bind(this))}>
      
-- on form submit:
1) handleSubmit is called
2) if everything is ok and ready to be subbmited, 
3) it then this.onSubmit.bind(this)) is called

-- we are calling bind here because we are passing this on submit as a callback function that will be executed in some different context outside of our component.

-- so to make sure we have access to the same this being essentially our component inside this thing we add on the bind this.

-- screenshot taken at 301 am --- all up to date -- genie local desktop

-- 

139. Form and Field States6:06

-- move back to validation
-- we see validation errors immediately
-- after we key in text we see the errors disappear
-- we dont want to show any error until they entered text and tabbed away
-- screenshot of mockup diagram at bam at 303 am

-- three different states of our form that we need to be aware of for each and every field
that we create.

-- PRISTINE = NO INPUT HAS TOUCHED IT AND THE USER HAS NOT YET SELECTED IT.
-- TOUCHED = A USER HAS SELECTED OR FOCUSED AN INPUT AND THEN FOCUSED OUT OF THE INPUT. YOU CAN IMAGINE THE USER HAS DONE SOME WORK ON THIS FIELD AND NOW CONSIDERS IT TO BE COMPLETE

-- INVALID = GOT SOME ERROR AND NEED TO SHOW IN SOME FASHION

-- SHOW MESSAGE ONLY IF ENTERED THE TOUCHED STATE:

--in renderField method
-- add ternary expression to field.meta:

FROM:
        {field.meta.error}

TO:

        {field.meta.touched? field.meta.error: ''}

--- all up to par and on track

-- succes ss on 309 at genie
E140. Conditional Styling7:06

-- show up red
-- get appropriate classnames generatting fields on text

-- apply has-danger to className of form-group

-- a new ternary expression when the user has touched it and an error exists

-- long segment before clenaup:

  const className = `form-group ${field.meta.touched && field.meta.error ? 'has-danger': ''}`;

-- use destrcuring off the meta propertry:

-- compacted syntax with destructoring, this does not get expanded into an object.

--it is just used for destructoring to pull off the properties touched and error from the meta object.


FROM: 
class PostsNew extends Component{

  const { meta } = field;
  const className = `form-group ${field.meta.touched && field.meta.error ? 'has-danger': ''}`;
  
  renderField(field){
    return(
      <div className="form-group has-danger">
        <label>{field.label}</label>
        <input
          className="form-control"
          type="text"
          {...field.input}
        />
        <div className="text-help">
          {field.meta.touched? field.meta.error : ''}
        </div>

      </div>
    );
    

FROM:

  const { meta } = field;
  const className = `form-group ${meta.touched && meta.error ? 'has-danger': ''}`;

TO:
    const { meta: {touched, error} } = field;
    const className = `form-group ${touched && error ? 'has-danger': ''}`;
    return(
      <div className={className}>
        <label>{field.label}</label>
        <input
          className="form-control"
          type="text"
          {...field.input}
        />
        <div className="text-help">
          {touched? error : ''}
        </div>

      </div>
    );

-- browser testing -- save & refresh in browser

-- test #1 
- when everything first renders I expect to see absolutely no error messages. 
- Status = PASS
--screenshot at -548 genie.local desktop

-- test #2
- now if i select or focus an input and I put in no text and focus to another one the entire thing turns red - 
- status = PASS
screenshot at -548 genie.local desktop


--test #3 
-- but if i go back into that input and enter in some text everything goes back to saying OK that looks like valid input 
- status = PASS
screenshot at 549/550 on genie.local 

-- you also notice that now, now that the user has kind of been messing around with this input a little bit they've put some text in here, 
now they will instantaneously get input or feedback the instant they start changing this thing around. 
-- so in practice, form renders pristine, everybody's happy.
-- but as soon as you start messing around with it,
OK we're going to start being pretty aggressive in showing you some validation messages.

-- next to make our submit button at the bottom actually submit this to our back end API.
-- we also need to make sure we show a cancel button on here that the user can click to go back to our list of posts.
141. More on Navigation3:11
-- ALL up to PAR and on TRACK

-- submit button gets wired up to action creator to create our posts
-- we also need a button to cancel the creation of a new post as well.

-- use the Link tag for navigating components

-- import link tag to posts_new.js
  import { Link } from 'react-router-dom';

 -- place Link tag inside of render function of posts_new.js:
   <Link to="/" className="btn btn-danger" >Cancel</Link>

-- test #4--
-- will cancel button work in browser
-- succes screenshot at genie.local desktop at 601 am

-- add space between these two buttons by adding margin-left:
  form a {
    margin-left: 5px;
  }
-- succes screenshot added 604 genie local desktop

142. Create Post Action Creator10:05

-- saving data via onSubmit Aciton Creator
-- creating action creator

FROM:
export default reduxForm({
  validate,
  form: 'PostsNewForm'
})(PostsNew);


TO: 
export default reduxForm({
  validate,
  form: 'PostsNewForm'
})(
  connect(null, { createPost }) (PostsNew)
);

-- test#5
-- post creates XHR request and uses requst method OPTIONS which means localhost to external for CORS

-- CORS is a security feature that is present inside your user's browser to present or prevent malicious type code from making requests to other domains.

-- screenshot taken at genie at 613 desktop

-- what we really care about itis the 2nd request which is the post request.

-- screenshot taken at 614 am on genie.local desktop

-- looks like we got back a status code of 201 created 

-- and if i click on the preview tab i see my category is content title and most importantly I have an ID as well.

-- success screenshot at genie.local desktop 616 am

--it looks like the post was successfully created!!
-- if we go back to the index page now the instant we go back to the index page, the index page will refetch our list of posts and we can now see the new post appear on the screen.

-- success screenshot at 617 (pressed submit twice --thats why theres two my posts)

-- looks like everything is working except this akward piece of flow

-- after submit, we want our user gets redirected automatically back to our list of posts.
-- screnshot taken at 619

-- so we need to somehow make sure that once the post has been created we actually navigate the user somewhere else.

-- all on track and on PAR.
143. Navigation Through Callbacks7:31
-- user mockup screenshot taken at bam at 621 -- shows flow affter user submits form

-- notice we wait and only after success, we navigate the user to the post list

-- this is called progammatic navigation 
-- we want to automatically navigate the user around our application the link tag is not for progammatic navigation.
-- the link tag is navigation that responds to a user clicking on something.
-- to handle progammatic, react-router passes in a big set of props on or into our component that is being read rendered by our route.
-- hey go back to our route:
        this.props.history.push('/');
-- only go back AFTER the post has been created:
    onSubmit(values){
      this.props.history.push('/');
      this.props.createPost(values);
   }
--  test# 6 - retest in browser to see if it goes back automatically

-- youll notice that because we navigated back to the index route before the post was created we entered into kind of a race condition where essentially that post is being created at the exact same time that we're fetching our list of posts.
-- so its a 50/50 chance as to whether or not our newly created post will actually show up on this list.

-- success screenshot at genie local desktop 629 am

-- screenshot shows post444 in XHR console but not list until refresh

-- success screenshot at 6:30 am on genie local desktop

-- screenshot shows post 444 on LIST and not in XHR console

-- we really have to wait here for the post to be created before we attempt to navigate back here.

-- we navigated too soon.

FROM: 

  onSubmit(values){
    this.props.history.push('/');
    this.props.createPost(values);
  }
  
TO:

  onSubmit(values){
    this.props.createPost(values, ()=> {
      this.props.history.push('/');
    });
  }

-- @COMEBACK AND UPDATE 
-- so the second argument im going to pass in a callback function and then im going to move the history.push call inside of that

-- so now our action creator has this function right here:

  onSubmit(values){
    this.props.createPost(values, ()=> {
      this.props.history.push('/');
    });
  }

-- if the action creator calls this function it will automatically navigate us back to our list of posts.

-- so now lets change over to our action creator file side of actions index and we'll go down to create posts right here [points to src/actions/index.js's createPost]
FROM:

export function createPost(values){
  const request = axios.post(`${ROOT_URL}/posts${API_KEY}`, values);

  return{
    type: CREATE_POSTS,
    payload: request
  }
}

TO:

export function createPost(values, callback){
  const request = axios.post(`${ROOT_URL}/posts${API_KEY}`, values);

  return{
    type: CREATE_POSTS,
    payload: request
  }
}

-- lets start off by 

-- so this is our callback function and now we want to make sure that only after this request right here has succeded, only after we have received this request or yo know only after the post has been created, do we want to call the callback manually to do so we can use a promise because that is what is returned by axios.post 

 [points to axios.post(`${ROOT_URL}/posts${API_KEY}`]

-- youre going to take the semi colon off the end and then on a new line we'll say:
FROM:
    const request = axios.post(`${ROOT_URL}/posts${API_KEY}`, values);

TO:

  const request = axios.post(`${ROOT_URL}/posts${API_KEY}`, values)
  .then(()=> callback());
  
-- then and inside of your we'll call the call back in practice:
--make the API request 
--after has been successfully completed
-- execute this function 
-- and all this function does is call the callback that we just passed in.

-- refresh in browser 

-- retest --- make post 5
-- ERROR no navigation --

screenshot taken before 645 on genie.local

Problem:
--noticed line 25 of index.js in actions had type: CREATE_POSTS instead of CREATE_POST
FROM:


  return{
    type: CREATE_POSTS,
    payload: request
  }
  
TO:


  return{
    type: CREATE_POST,
    payload: request
  }

-- still no navigation

-- order of operations SHOULD be at button click submit:

-- we get the response back 
-- and then we navigate to our list of posts so submit and there we go.

-- noticed an error at index.js of action creators. no callback passed to createPost.

FROM:

export function createPost(values){
  const request = axios.post(`${ROOT_URL}/posts${API_KEY}`, values)
  .then(()=> callback());

  return{
    type: CREATE_POST,
    payload: request
  }
}


TO:

export function createPost(values, callback){
  const request = axios.post(`${ROOT_URL}/posts${API_KEY}`, values)
  .then(()=> callback());

  return{
    type: CREATE_POST,
    payload: request
  }
}

-- SUCCES SCRENSHOT TAKEN At 651 -- 

--all on track and on PAR


144. The Posts Show Component3:39

-- find post with id 5

-- scaffolding for new compnent

--posts_show.js

--import react

-- extend compnent

-- render

--return a div of posts show

-- export default postsshow

import React, { Component } from 'react';

class PostsShow extends React.Component {
  render(){
    return(
      <div>
        Posts Show!
      </div>
    );
  };
}
export default PostsShow;

-- QUESTION #1: When do you know when to end a code "block" with a semicolon? When to use after a (); and when to use after a {}; ?

- QUESTION #2:Does it matter when you render return with curly braces or parenthesis? Does it matter when you render(){return(<div>Posts Show! </div>) vs render(){return{<div> Posts Show! </div>}}}
In the render's return, what is the difference when you use parenthesis:

class PostsShow extends React.Component {
render(){return(<div> Posts Show! </div>)} 

versus when you use curly braces:

class PostsShow extends React.Component {
render(){return{<div> Posts Show! </div>}}

​question #3 PostShow extends React.Component vs PostsShow extends Component:
When creating a new component, is it ever useful to extends React.Component{} instead of extends Component?

Will there be that much of a file size reduction and performance boost if I always used extends Component?

Is it just for the purpose of code golf to use extends Component?

Which is better?

Is this stronger typing ever useful?

If so, could you give an example of when using 

extends React.Component 

 is better than using 

extends Component 

Thank you for your time and attention!

-- add this to a new route component

--import the component we just created in the index.js of trhe src root:
   import PostsShow from './components/posts_show';

-- add in an additional route in the <switch> block

-- REMEMBER: THE ORDER IN WHICH WE DEFINE OUR ROUTES MAKES A BIG DIFFERENCE IN THE REACTDOM.RENDER(PROVIDER>BROWSERROUTER>DIV>SWITCH> ROUTE)
-- IF WE DEFINE ROUTES IN AN INCORRECT ORDER WE MIGHT MATCH AN INCORRECT ROUTE AND WELL GET THE INCORRECT COMPONENT TO APPEAR ON THE SCREEN.

-- So in this case, we want to make sure that we add this new route between the two existing ones:

          <Route path="/posts/new" component={PostsNew} />
                    H E R E
          <Route path="/" component={PostsIndex} />
          


FROM:

  <Provider store={createStoreWithMiddleware(reducers)}>

    <BrowserRouter>
      <div>
        <Switch>
          <Route path="/posts/new" component={PostsNew} />
          <Route path="/" component={PostsIndex} />
        </Switch>
      </div>

    </BrowserRouter>
  </Provider>

TO:
  <Provider store={createStoreWithMiddleware(reducers)}>

    <BrowserRouter>
      <div>
        <Switch>
          <Route path="/posts/new" component={PostsNew} />
          <Route path="/posts/:id" component={PostsShow} />
          <Route path="/" component={PostsIndex} />
        </Switch>
      </div>

    </BrowserRouter>
  </Provider>
  
-- REMEMBER: THAT THE COLON ID RIGHT HERE IS A WILD CARD OF SORTS. SO REACT ROUTER IS GOING TO TRY TO TAKE WHATEVER IS IN THAT LITTLE POSITION URL AND PASS IT AS AS PROPERTY OR A PROP TO OUR POST SHOW COMPONENT.

-- We wanted to make sure that this was specifically the second route inside of our application because if it were the first one, if the user tried to navigate to posts/new, /new would be taken as the wildcard token. 
-- and so this route would match PostsNew if it was first
-- so thats why we wanted to make sure that it is the second one inside of our application.

-- save file and refresh browser to test

-- navigate to posts manually posts/123:
  localhost:8080/posts/123

-- succes screenshot taken at 801 at genie local desktop
--we correctly see posts show ont he screen and if we go to /new we still see the new form on the screen. 


  localhost:8080/posts/new

-- screenshot taken at genie local desktop 802 am


F145. Receiving New Posts9:26

-- one concept underlying of the creation of new posts
-- it all comes down to how we load our data inside of our application really quick
-- mockup screenshot from bam taken at 805 am
-- screenshot shows redux flow

-- two types of flow

-- user visits postindex first -> action creators create postss state withe posts 1 2 and 3.

--user visits postsshow first -> action creators create posts state with just post 2
-- so if a user goes directly to the postshow component we want to only fetch the data that is required.
-- but if a user lands on our application by going to the postsindex page we watch to fetch everything thats available.

-- its really important to keep in mind that a user can enter into your application on pretty much absolutely any page they want by either bookmarking the page or maybe they open up a new tab or maybe they share a link with a friend.

-- you always have to assume that a user might be entering to any given page inside of your application.

-- what hes trying to say is the postsshow component really needs to be responsible for fetching its own data.
-- we cannot assume that the user first went to the posts index page and fetched the big lists of posts and then navigated it over to post 
-- so we have to always assume that the user or 
we need to fetch fresh data for the user whenever the user comes to this component 

-- start off new component by putting together an action creator to go and fetch a very particular post 

-- inside of posts show component 

-- goal is to first create an action creator to create a new post

-- define new action creator:
  export function fetchPost(id){
  
  }

-- form up axios.get api request to get data

-- this is the type of route we want to end up with (per the api):
  http://reduxblog.herokuapp.com/api/posts/5

-- fetch_post action creeator:

export function fetchPost(id){
  const request = axios.get(`${ROOT_URL}/posts/${id}${API_KEY}`);
  return{
    type: FETCH_POST,
    payload: request
  };
}

--update the export const for the action creators :

export const FETCH_POSTS = 'fetch_posts';
export const FETCH_POST = 'fetch_post';
export const CREATE_POSTS = 'create_posts';


-- go back to reducer and add in a case to catch this new type and add it to our application level state

-- update import to actions in reducer_posts:
FROM: 

import { FETCH_POSTS } from '../actions';


TO:

import { FETCH_POSTS, FETCH_POST } from '../actions';

-- add an additonal case:

FROM:

export default function(state = {}, action){
  switch(action.type){
    case FETCH_POSTS:
      return _.mapKeys(action.payload.data, 'id');
    default:
      return state;
  }
}


TO:

import _ from 'lodash';
import { FETCH_POSTS, FETCH_POST } from '../actions';

export default function(state = {}, action){
  switch(action.type){
    case FETCH_POST:
      const post = action.payload.data;
      const newState = { ...state };
      newState[post.id] = post;
      return newState;
    case FETCH_POSTS:
      return _.mapKeys(action.payload.data, 'id');
    default:
      return state;
  }
}

COMMENT OUT BEFORE (ES6)

      // const post = action.payload.data;
      // const newState = { ...state };
      // newState[post.id] = post;
      // return newState;
      

TO (IN ES6 identitcal)

      return {...state, [action.payload.data.id]: action.payload.data};

FULL:

import _ from 'lodash';
import { FETCH_POSTS, FETCH_POST } from '../actions';

export default function(state = {}, action){
  switch(action.type){
    case FETCH_POST:
      return {...state, [action.payload.data.id]: action.payload.data};
    case FETCH_POSTS:
      return _.mapKeys(action.payload.data, 'id');
    default:
      return state;
  }
}

-- same exact thing as what we're doing in these four lines of code we commented out.

-- REMEMBER: WHEN USING SQUARE BRACES/BRACKETS HERE, THIS IS NOT AN ARRAY. THIS IS IS NOT AN ARRAY HERE:
      return {...state, [action.payload.data.id]: action.payload.data};

-- WE ARE USING KEY INTERPOLATION
-- SO WE'RE SAYING WHATEVER THE VARIABLE ACTION PAYLOAD.DATA.ID IS, MAKE A NEW KEY ON THIS OBJECT USING THIS VALUE RIGHT HERE [POINTS TO ACTION.PAYLOAD.DATA.ID] AND SET ITS VALUE EQUAL TO ACTION.PAYLOAD.DATA [POINTS TO OTHER SIDE OF COLON FOR RETURN STATEMENT ].

            return {...state, [action.payload.data.id]: action.payload.data};

-- So over time as a user starts to fetch more show routes inside of our application, we'll fetch each of these additional posts and we'll add them into the overall state object right here. points to
            return {...state, [action.payload.data.id]: action.payload.data};

-- so in this section we put together our fetch post action creator and we also added a bit of logic to our reducer to meld that new post into our application level state.

-- next is to make sure the posts show component will actually call that action creator.
146. Selecting from OwnProps11:27
-- in posts_show.js start by importing help connector from react-redux and 
  import { connect } from 'react-redux';

-- import fetchpost from actions  import { fetchPost } from '../actions';
-- hook this up to connect helper on export default
FROM:
  export default PostsShow;

TO: 
  export default connect(null, { fetchPost })(PostsShow);

-- we update the PostsShow to have a lifecycle method like before.

-- so now the instant this component appears on the screen we're going to reach out and fetch that post

-- presumably the action creator will fetch that post youll get added to our post piece of state and that means we then need to take that post out of our application level state and get it into our component with a map state to props function.

-- we need to know the ID that sits in the URL 

-- that URL is a very important piece of state because its going to dictate exactly how this component behaves.

-- so to get access to that URL or the little token thats inside that URL I should say,
we will make access to a prop from that is provided to us from react router

-- so up inside of the componentDidMount, we can access this.props.match.params.id; 
-- we get this.props.match.params.id directly provided by react router 
-- with react router, the match right here is the top level property:
 this.props.match.params.id; 

-- the params property inside of it is an object that lists all the different wildcard tokens that exist inside the URL.

-- so if we go back to the src  index.js file and we find our route's definition we're not only limited to having one wildcard inside the URL right here
-- we could just as easily have maybe a comment Id as well, if we wanted to look up a very particular comment if you know we imagine we had comments 

  <Route path="/posts/:id/:commentId" component={PostsShow}>-- so that params object will contain all the different wildcard values that exist inside of our given URL

-- in this case we only have the ideal one an so of course we're just saying yep we just want to get access to the ID out of the URL.

-- again, we need to make sure that this id gets passed to fetch post right here [points to componentDidMount of posts_show.js]

-- he thinks it would be appropriate to assign this to a variable right above it. using a little bit a destructoring:

	const { id } = this.props.match.params;
        this.props.fetchPost(id);

-- this takes care of fetching an individual post of telling that action creator hey I want a post with this given ID

-- update mapstatetoprops to return { posts }

-- and then inside of the render function because post is this big list of posts we might do something like posts with this.props.match.params.id and that would result in the post we want to show:
      posts[this.props.match.params.id]


-- so you might be thinking yea lets just use mapStateToProps in a similar way there were always used to 

-- REMEMBER: NO BIG DEAL. JUST GO FOR IT!

-- NEW TRICK THIS TIME TO CLEAN UP A LOT OF THE LOGIC INSIDE OF YOUR COMPONENT AND ENABLING YOU WRITE THEM IN A MORE REUSABLE FASHION.

-- THIS LINE EXPECTS WE ARE GOING TO GET THIS HUGE LIST OF POSTS:
    posts[this.props.match.params.id]

-- however the component really only cares about a very particular post only one individual single post.

-- so rather than passing the big list of posts into this component im going to suggest that we figure out a way instead to only pass in a single post. just the one that we care about.

-- so thats the goal here: I want to say I dont want to make this component rely on a big list of posts. 

-- I want it to always expect to recieve one single component so im going to clean up this line of code [deleted [posts[this.props.match.params.id] and return statement inside of mapstateto props as well]]. 

-- here's the trick we're going to do to make this a little bit more reusable

-- heres our map state to props function and we've said so many times that the first argument to it is our application state but there is a second argument.

-- the second argument is referred to by convention as ownProps.

FROM:
function mapStateToProps( { posts }){

}
TO:
function mapStateToProps( { posts }, ownProps ){

}

-- OwnProps right here is the props objet that is headed or going to this component [points to posts_show class extends component block without function mapStateToProps]

-- so whenver this component is about to be rendered or rerendered on the screen, 
REMEMBER: mapStateToProps GETS CALLED TO FIGURE OUT WHAT PROPS THE COMPONENT NEEDS AND mapStateToProps is passed all the props that were headed to post show.

-- to put that another way, we could essentially say inside of here [points to render of posts_show between render and return]:
  this.props === ownProps
-- says this.props is absolutely equal to own props

-- he removes it immediately after entering it

-- consider that then realize we can return just the single post that we care about which would be posts ownProps match.params.id:

FROM:
function mapStateToProps( { posts }, ownProps ){

}
TO:
  function mapStateToProps( { posts }, ownProps ){
    return {post: posts[ownProps.match.params.id] };
  }

-- so now our component is only ever going to recieve the single post that we care about just this one post and not the big list.

-- you might be saying stephen thats so ridiculous we talk about here we still are dealing with a big list of posts inside of this component right here [ppints to posts in return ]

-- we're still dealing with the big list of posts inside the map state to props... whats the difference?

-- well there is a difference in many large applications, its not entirely uncommon to create your map state to props functions in a separate file 

-- so have a completely separate map state to props function completely separate from the actual component.

-- if we had taken that type of approach inside of this application, and said map state to props and a second file and this would only contain PostsShow.

-- thats way more reasonable to say yea this things starts to get more reusable.

-- all of a sudden postsShow can be responsible for just showing a component and really not doing much else.

-- and so it doesnt have that additional data dependecny of getting the big list of posts.

-- and if nothing else it helps to just clean up the actual component right here.
-- and he thinks it kind of lessens the mental burden of remembering o yeah OK thats abig list of posts, I need to just access the one I really care about.

-- so maybe if our render method needed to refer to the post, we could say:
  render(){
    this.props.post 
   return (
   )

-- and if we had a helper function we could just say this.props.post which is way more compact than doing something like you know something like this in both locations far more compact far more legible than the otther apprach:

FROM:
class PostsShow extends React.Component {
  componentDidMount(){
    const { id } = this.props.match.params;
    this.props.fetchPost(id);
  }
  helperFunction(){
    this.props.post;
  }
  render(){
    this.props.post;
    return(
      <div>
        Posts Show!
      </div>
    );
  };
}

function mapStateToProps( { posts }, ownProps ){
  return {post: posts[ownProps.match.params.id] };
  
TO:

class PostsShow extends React.Component {
  componentDidMount(){
    const { id } = this.props.match.params;
    this.props.fetchPost(id);
  }
  helperFunction(){
    this.props.posts[this.props.match.params.id];
  }
  render(){
    this.props.match.params.id;
    return(
      <div>
        Posts Show!
      </div>
    );
  };
}

function mapStateToProps( { posts }, ownProps ){
  return {post: posts[ownProps.match.params.id] };
}

-- above approach is bad and goes back to original by deleting line between render and reutnr and helper funciton.
 
-- important technique to remember

-- REMEMBER: WE CAN USE MAP STATE TO PROPS NOT JUST TO SELECT LITTLE PIECES OF STATE OFF THE GLOBAL STATE OBJECTS BUT ALSO DO SOME INTERMEDIATE CALUCLATION OF SORTS INSIDE AS HERE AS WELL [POINTS TO RETURN {POST: POSTS[]'}]

-- so the last step we have to do is to pass in map state to props to the connect funciton

FROM:

export default connect(null, { fetchPost })(PostsShow);

TO:

export default connect(mapStateToProps, { fetchPost })(PostsShow);

-- screenshot at bam taken at 933 showing the semi colon at the end of the return statement. says its his mistake.

-- another screenshot taken at bam 934 to show both semi colons in render and return of posts_show.js

FROM:
  render(){
    return(
      <div>
        Posts Show!
      </div>
    );
  };
  
TO:

  render(){
    return(
      <div>
        Posts Show!
      </div>
    );
  }
147. Data Dependencies5:32-- the last thing that we have to do inside of our post show component is take the post we were seeing as a prop and show it inside the render funciton.

-- so rather than showing the hard coded text of Posts Show! , we'd like to show the post title categories all that kinda good stuff.

-- use alittle bit of markup to show details about the particular post

-- because we're going to refer back to ths post a couple of times,
 use some destructoring
 -- so we'll say const post is coming from this.props than inside
 
--update render of posts_show:
  render(){
    const { post } = this.props;
    return(
      <div>
        <h3>{post.title}</h3>
        <h6>Categories:{post.categories}</h6>
        <p>{post.content}</p>
      </div>
    );
  }
  

-- why did we use a <p> paragraph tag for post.conent?
-- when we render this component in the browser,
we should reach out to fetch the given post.

-- once we get the post back, 
we select it from the post object. (thats our application state)

-- then we will render some details about it on the screen

-- save and test in browser

-- first we need to make sure we render a post that we have an Id for

-- inside of network console, i need to refresh the page while im specifically looking at my list of posts, look at an individual request, find the ID for one of my existing posts on this list.

-- screenshot of succes on genie.local destop at 944amm

ex:  id: 147217

-- test -- i should be able to navigate to post 147217:

    localhost:8080/posts/147217
    
-- do make sure that youre using a very real post ID right here
-- if you are not using a real post id ou wil lnot see anythgin appear on the screen

--test it out localhost:8080/posts/147217

-- EXPECTED FAILURE/ERROR
  
-- ERROR SCREENSHOT AT 947 AT GENIE.LOCAL DESKTOP

--ERROR: Uncaught TypeError: Cannot read property 'title' of undefined

t PostsShow.render (bundle.js:51497)
    at ReactCompositeComponentWrapper._renderValidatedComponentWithoutOwnerOrContext (bundle.js:7803)
    at ReactCompositeComponentWrapper._renderValidatedComponent (bundle.js:7823)
    at ReactCompositeComponentWrapper.wrapper [as _renderValidatedComponent] (bundle.js:1554)
    at ReactCompositeComponentWrapper.mountComponent (bundle.js:7436)
    at ReactCompositeComponentWrapper.wrapper [as mountComponent] (bundle.js:1554)
    at Object.mountComponent (bundle.js:5746)
    at ReactCompositeComponentWrapper.mountComponent (bundle.js:7441)
    at ReactCompositeComponentWrapper.wrapper [as mountComponent] (bundle.js:1554)
    at Object.mountComponent (bundle.js:5746)
render @ bundle.js:51497
_renderValidatedComponentWithoutOwnerOrContext @ bundle.js:7803
_renderValidatedComponent @ bundle.js:7823
ReactCompositeComponent__renderValidatedComponent @ bundle.js:1554
mountComponent @ bundle.js:7436
ReactCompositeComponent_mountComponent @ bundle.js:1554
mountComponent @ bundle.js:5746
mountComponent @ bundle.js:7441
ReactCompositeComponent_mountComponent @ bundle.js:1554
mountComponent @ bundle.js:5746
mountComponent @ bundle.js:7441
ReactCompositeComponent_mountComponent @ bundle.js:1554
mountComponent @ bundle.js:5746
mountComponent @ bundle.js:7441
ReactCompositeComponent_mountComponent @ bundle.js:1554
mountComponent @ bundle.js:5746
mountChildren @ bundle.js:14316
_createContentMarkup @ bundle.js:11491
mountComponent @ bundle.js:11379
mountComponent @ bundle.js:5746
mountComponent @ bundle.js:7441
ReactCompositeComponent_mountComponent @ bundle.js:1554
mountComponent @ bundle.js:5746
mountComponent @ bundle.js:7441
ReactCompositeComponent_mountComponent @ bundle.js:1554
mountComponent @ bundle.js:5746
mountComponent @ bundle.js:7441
ReactCompositeComponent_mountComponent @ bundle.js:1554
mountComponent @ bundle.js:5746
mountComponent @ bundle.js:7441
ReactCompositeComponent_mountComponent @ bundle.js:1554
mountComponent @ bundle.js:5746
mountComponentIntoNode @ bundle.js:2750
perform @ bundle.js:6853
batchedMountComponentIntoNode @ bundle.js:2766
perform @ bundle.js:6853
batchedUpdates @ bundle.js:10890
batchedUpdates @ bundle.js:6358
_renderNewRootComponent @ bundle.js:2960
ReactMount__renderNewRootComponent @ bundle.js:1554
_renderSubtreeIntoContainer @ bundle.js:3034
render @ bundle.js:3054
React_render @ bundle.js:1554
(anonymous) @ bundle.js:94
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:47
__webpack_require__ @ bundle.js:20
(anonymous) @ bundle.js:40
(anonymous) @ bundle.js:43
util.js:228 Google Maps API warning: NoApiKeys https://developers.google.com/maps/documentation/javascript/error-messages#no-api-keys
UB.j @ util.js:228
(anonymous) @ js:140
(anonymous) @ js:63
(anonymous) @ js:61
(anonymous) @ js:63
(anonymous) @ js:116
(anonymous) @ js:61
(anonymous) @ js:116
(anonymous) @ js:61
(anonymous) @ js:116
fe @ js:63
ee.na @ js:116
(anonymous) @ util.js:1
js:40 Google Maps API error: MissingKeyMapError https://developers.google.com/maps/documentation/javascript/error-messages#missing-key-map-error
_.Ub @ js:40
(anonymous) @ common.js:51
(anonymous) @ common.js:193
c @ common.js:45
(anonymous) @ AuthenticationService.Authenticate?1shttp%3A%2F%2Flocalhost%3A8080%2Fposts%2F147217&callback=_xdc_._vd61re&token=107726:1

-- should see something about cannot read property title of undefined.

-- whats going on here [look at posts_show commponent]

-- think about order of operations

-- when this is component is first rendered to the screen,

it then calls the componentDidMount gets called to fetchour post

--then once we fetch post, redux,,, connect...compnent rerenders and shows details ont he screen.

-- they key is the first part of the flow - the component is rendered one time before its fetched our first post.

-- during that time before we even attempted to fetch our post we dont have any post with the correct ID sitting in memory.

-- so when we tried to reach into oru big object containing all these posts this satement down here return { post: posts [ownProps..]} will return undefined.

-- and so post of undefined will be passed into our aplpication or into our component.

-- and so we are literally trying to look at the property title of undefined essentially post right here is coming in as undefined to our application [points to const {post} of render method in posts_show.js]

-- to resolve this we can add a little bit of a check to our render method inside of here before we try to access any of the nested properties on the post itself.

-- we can look at the post and we can say hey if we dont have one, 
how bout instead of trying to return this big blockof JSX down here, 
lets just return a div that contains the text loading... like so:

-- so now if we render this component when a post has not yet been fetchd correcltly, we'll show the loading div and then once the post is fetched and this component renders, we will then have a post available and will hit this block of JSX instead [points to return post title etc].

  render(){
    const { post } = this.props;

    if (!post){
      return <div>Loading...</div>;
    }
    return(
      <div>
        <h3>{post.title}</h3>
        <h6>Categories: {post.categories}</h6>
        <p>{post.content}</p>
      </div>
    );
  }
  
-- save and refresh browser to test to see if we see the post appear on the screen

http://localhost:8080/posts/147217

-- success screenshot on genie.local at 959

-- all on track and on PAR

-- he wants to let me know that data issues like this where you would try to access properties on an element or a record that does not yet exist is something that you are going to run up against inside of react and redux just all the time on your personal projects. I guarantee you are going to run into this issue right here.

-- so whenever you start to see messages appear on the screen like cannot read property title is undefined, do double check to make sure that the record youre trying to access actually exists. 

-- and if it does not, you can add in a simple check to say well if we dont have that data yet no problem just do something else.



148. Caching Records6:13--the last two things
1- make Back to index button
- update posts_show with link tag from react-router-dom.
- inside of render function, place a linked tag we'll tell it to render the user or something.
- refreshin the browser to test
-- sucess screenshot taken at genie llcoal desktop 1006 am


2- make back button
-- lets make sure the user has the ability to navigate from clicking right here and going to the show page for each particular or each particular post.

-- again, were going to use the link tag inside of our post index component

-- since we already imported the Link tag, 
we just wrap the post title insode of the render post function with another link:

        <li className="list-group-item" key= {post.id}>
          <Link to={`/posts/${post.id}`}>
            {post.title}  
          </Link>
          
-- save and  test this inside of browser
-- sUCCES SCREENSHOT at genie at 1011 and 1012

-- notice we are fetching each record TWICE (once for the index page) and (once for the show page)

-- he says for me personally, that is how I always construct pages I always assume that we're working with stale data becauase you never know how long a user has been sitting at this index page.

-- and so i always want to refetch records whenever i go to the show page.

-- if you are working on an application and you are really really concerned about network usage, you could always add a check inside of the post show component.

-- goto posts_show.js and look at componentdid mount 

-- if you did not want to eagerly refetch posts you can always wrap this thing with an if statement. [points at component did mount] 

  componentDidMount(){
    if (!this.props.post){
      const { id } = this.props.match.params;
      this.props.fetchPost(id);
    }
  }
  
-- test to see if it works in the browser

-- success screnesnhot at genie at 1019 showing one fetch instead of two


-- COMEBACK AND EXPLAIN WHY ITS SO FAST
-- ON TRACK AND ON PAR
149. Deleting a Post9:25-- screenshot at bam at 1021 of mockup of delete post button

-- 

  onDeleteClick(){
    const { id } = this.props.match.params;
    this.props.deletePost(id);
  }
  
could do it this way bad

  onDeleteClick(){
    const { id } = this.props.match.params;
    this.props.deletePost(this.props.post.id);
  }
  
-- its bad approach because it assumes that they post is in existence inside this component.
-- it assumes we have fetched the posts already
-- this component here will render on the screen without the post being availalble.
-- so he thinks its a bit more risky to refer to the post on props. its way more reasonable to look at params object.
-- the params object is always going to have the ID available and so we dont really ever have to think about it at all.

-- we are working backwards here, 
-- we are going to continue this kind of backwards flow by importing the action creator from the actions file:

import { fetchPost, deletePost } from '../actions';

--now were going to wire it up to our connect helper at the bototm of the file.

-- update acitons.js


--define export function deletePost

export function deletePost(id){
  const request = axios.delete(`${ROOT_URL}/posts/${id}${API_KEY}`);
  return{
    type: DELETE_POST,
    payload: id
  };
}

--navigate user back to post after delete

export function deletePost(id, callback){
  const request = axios.delete(`${ROOT_URL}/posts/${id}${API_KEY}`)
  .then(() => callback());
  
and 
class PostsShow extends React.Component {
  componentDidMount(){
    //optional to leave out for stale data vs network usage concerns
    if (!this.props.post){
      const { id } = this.props.match.params;
      this.props.fetchPost(id);
   }
  }
  onDeleteClick(){
    const { id } = this.props.match.params;
    this.props.deletePost(id, ()=> {
      this.props.history.push('/');
    });
  }
  
-- save and retest in browser to see if we can go back to list of posts, refresh the page and click on post to see big red button the side for delete post, click the button, see the post required or the delete request come up and then automatically navigate back to the index.

-- screenshot success at genie local 1038 and 1039
-- delete post works!

-- expected error in console

--ERROR: 
bundle.js:49676 Uncaught ReferenceError: DELETE_POST is not defined
    at deletePost (bundle.js:49676)
    at Object.deletePost (bundle.js:21191)
    at PostsShow.onDeleteClick (bundle.js:51514)
    at Object.ReactErrorUtils.invokeGuardedCallback (bundle.js:4556)
    at executeDispatch (bundle.js:4356)
    at Object.executeDispatchesInOrder (bundle.js:4379)
    at executeDispatchesAndRelease (bundle.js:3809)
    at executeDispatchesAndReleaseTopLevel (bundle.js:3820)
    at Array.forEach (<anonymous>)
    at forEachAccumulated (bundle.js:4656)
deletePost @ bundle.js:49676
(anonymous) @ bundle.js:21191
onDeleteClick @ bundle.js:51514
ReactErrorUtils.invokeGuardedCallback @ bundle.js:4556
executeDispatch @ bundle.js:4356
executeDispatchesInOrder @ bundle.js:4379
executeDispatchesAndRelease @ bundle.js:3809
executeDispatchesAndReleaseTopLevel @ bundle.js:3820
forEachAccumulated @ bundle.js:4656
processEventQueue @ bundle.js:4025
runEventQueueInBatch @ bundle.js:4685
handleTopLevel @ bundle.js:4701
handleTopLevelWithoutPath @ bundle.js:14907
handleTopLevelImpl @ bundle.js:14887
perform @ bundle.js:6853
batchedUpdates @ bundle.js:10890
batchedUpdates @ bundle.js:6358
dispatchEvent @ bundle.js:15018

-- on track and on par


G150. Wrapup9:10-- update top of action creator

FROM:


export const FETCH_POSTS = 'fetch_posts';
export const FETCH_POST = 'fetch_post';
export const CREATE_POSTS = 'create_posts';


TO:

export const FETCH_POSTS = 'fetch_posts';
export const FETCH_POST = 'fetch_post';
export const CREATE_POSTS = 'create_posts';
export const DELETE_POST = 'delete_post';



-- save and rest in browser

-- SUCCESS SCREENSHOT at genie.loca at 1041 desktop showing no error in console and clean network XHR traffic

-- snappier uI - lets handle it better

-- import delete post

-- lodash omit -- what it does right here is says look at the state object.
if the state object has a key of the posts id jsut drop it
-- just omit it from the object and return a new object that does not contian that id anymore
-- so this does not modify the existing state object and returns a new state object with that particular post id not present anymore

-- so this is part of whats so great about using an object rather than array for state management.

-- you can imagine i fyou are using an array here we ould have to write in a reject funciton
      return _.reject(state, post => post.id === action.payload);
      
-- above is definatley not quite as legible
-- omit is more obvious as to whats going on - and actually this would be post ID

-- so i personally like using an object as our application level state

-- save and refresh browser to retest to see if we will delete this post and right away we see that things just get out there and we're good to go.

-- succes screenshot at genie at 1049 and 1050 and 1051 showing the refresh, the page for post detail and deleting the post. with no errors in console

-- @COME BACK AND GET WRAP UP 

-- peep some javascript library called reselect

-- peep bonus video about fine detailing applicaiton state.




151. Rallycoding0:00--

RallycodingSection 9, Lecture 151Be sure to check out RallyCoding.  You'll find a lot of helpful blog posts, new courses, and all kinds of other stuff!Interested in any of my other courses?  Pick them up for just $10!React Native: Advanced Concepts - https://www.udemy.com/react-native-advanced/?couponCode=4MORE1234GraphQL With React: The Complete Developer's Guide - https://www.udemy.com/graphql-with-react-course/?couponCode=4MORE1234Webpack 2: The Complete Developer's Guide - https://www.udemy.com/webpack-2-the-complete-developers-guide/?couponCode=4MORE1234MongoDB with NodeJS - https://www.udemy.com/the-complete-developers-guide-to-mongodb/?couponCode=4MORE1234Elixir with Phoenix - https://www.udemy.com/the-complete-elixir-and-phoenix-bootcamp-and-tutorial/?couponCode=4MORE1234ES6 Javascript - https://www.udemy.com/javascript-es6-tutorial/?couponCode=4MORE1234Meteor with React for Realtime Apps - https://www.udemy.com/meteor-react-tutorial/?couponCode=4MORE1234Advanced React with Redux - https://www.udemy.com/react-redux-tutorial/?couponCode=4MORE1234Electron for Desktop Apps - https://www.udemy.com/electron-react-tutorial/?couponCode=4MORE1234-- APP DONE FINAL COMMIT-=--==-=

code Rally:

Bonus - RallyCoding100. Basics of Redux Thunk7:16
-- why thunk exist
-- the purpose of thunk
-- the purpose of redux itself is to hold our application state.
-- mockup screenshot taken at bam at 1140 showing react + redux dispatch cycle.
-- its a pattern that we repeat over and over in our applications.
-- this pattern works for things that are synchronous
-- synchronose means an action in which instantly flows into our middleware and our reducers 

-- the vast majority of web applications we build however need to fetch data through asynchronous channels.
-- in other words, its much more common that when we call an action creator we actually want to go and fetch some amount of data from some API or you know some asynchronous action and only when that request resolves are we actually ready to create an action. 
-- vanilla redux is not set up for this type of operation right out of the box.
-- so how do we handle these asynchronous action creators?
-- how do we make asynchronous requests?
-- thats where redux thunk comes into play
-- the purpose of redux thunk is to give us direct control over the dispatch method

101. Combining Redux and Firebase12:16

102. Dynamic Forms with Redux Form14:42

103. Logicless Components with Reselect18:08104. Data Loading Methods with Redux9:29105. Animation of React Components12:33106. Four Most Common Errors with React and Redux12:02107. Modals in React and Redux Apps18:43108. The Best Way to Store Redux Data15:05109. BrowserHistory in Production19:46110. Introducing JSPlaygrounds for Rapid Prototyping12:18111. Deployment of React/Webpack Apps23:15112. React Integration with Third Party Libraries18:42