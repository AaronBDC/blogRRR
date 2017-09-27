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


133. Setting Up Redux Form9:27134. The Field Component10:49D135. Generalizing Fields8:54136. Validating Forms10:31137. Showing Errors to Users4:30138. Handling Form Submittal9:30139. Form and Field States6:06E140. Conditional Styling7:06141. More on Navigation3:11142. Create Post Action Creator10:05143. Navigation Through Callbacks7:31144. The Posts Show Component3:39F145. Receiving New Posts9:26146. Selecting from OwnProps11:27147. Data Dependencies5:32148. Caching Records6:13149. Deleting a Post9:25G150. Wrapup9:10151. Rallycoding0:00