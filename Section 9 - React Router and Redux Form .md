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
124. State as an Object9:07


B125. Back to Redux - Index Action7:07126. Implementing Posts Reducer10:29127. Action Creator Shortcuts8:06128. Rendering a List of Posts9:19129. Creating New Posts5:42C130. A React Router Gotcha4:44

131. Navigation with the Link Component5:58132. Redux Form5:33
133. Setting Up Redux Form9:27134. The Field Component10:49D135. Generalizing Fields8:54136. Validating Forms10:31137. Showing Errors to Users4:30138. Handling Form Submittal9:30139. Form and Field States6:06E140. Conditional Styling7:06141. More on Navigation3:11142. Create Post Action Creator10:05143. Navigation Through Callbacks7:31144. The Posts Show Component3:39F145. Receiving New Posts9:26146. Selecting from OwnProps11:27147. Data Dependencies5:32148. Caching Records6:13149. Deleting a Post9:25G150. Wrapup9:10151. Rallycoding0:00