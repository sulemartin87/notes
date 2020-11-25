## vue3 is vue next,
vue core is complete 
router and vuex integration in devtools is not complete
that's why vue2 
npm will still install vue2 
use vue@next to get vue3


changes 

vue is created with createApp now 
data must always be a method 
components, directives and third party modules are resitered on app instead of vue global object 
v-enter is now v-enter-from 
vue router is created iwth createRouter 
vuex is now created with createStore()

new 
teleport component 
fragments 
composition api / optional 
vue has better support with typescript 
[examples](https://github.com/academind/vue-3-update/tree/vue3-update)


## vue 3 emits

have an event for sending event 
have another for done 
can listen to each one 

@sending = "started // a function"
define a function for a value

define them in the emits components 

you can validaate an event 

define it in an object of emits

