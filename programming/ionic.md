## useful stuff 

ionic -vue 
preferably use typescript but can remove typsecript // check docs

defaults to vue3 //docs are vue3

To use a component in Vue, you must first import it. So for Ionic Framework, this means anytime we want to use a Button or a Card, it must be added to our imports. In the case of our App component, we are using IonApp and IonRouterOutlet. You can also register components globally if you find yourself importing the same components repeatedly. This comes with performance tradeoffs that we cover in [Optimizing Your App](https://ionicframework.com/docs/vue/quickstart#optimizing-your-app).

router is exactly the same as vue

> ionPage is root component 
>> has header, title, and content components 
```
When creating your own pages, do not forget to have IonPage be the root component for them. Having IonPage be the root component is important because it helps ensure transitions work properly as well as provides the base CSS the Ionic Framework components rely on. 
```
