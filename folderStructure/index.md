# Large Scale Vue Application Structure

### Application Structure LIFT Principle

* Locating our code is easy
* Identify code at a glance
* Flat structure as long as we can
* Try to stay DRY (Don’t Repeat Yourself) or T-DRY

### "Folders-by-Feature" Structure

Create folders named for the feature they represent. When a folder grows to contain more than 7 files, start to consider creating a folder for them. Your threshold may be different, so adjust as needed.

### Why?

* A developer can locate the code, identify what each file represents at a glance, the structure is flat as can be, and there is no repetitive nor redundant names.
* The LIFT guidelines are all covered.
* Helps reduce the app from becoming cluttered through organizing the content and keeping them aligned with the LIFT guidelines.
* When there are a lot of files (10+) locating them is easier with a consistent folder structures and more difficult in flat structures.

### Example Application Structure

```
├─ src
├── assets
├── components
│   └─ ResusableComponentA
│       ├─ index.js
│       ├─ ReusableComponentA.vue
│  		└─ ReusableComponentA.spec.js
├── lang
│   └─ index.js
├── mixins
│   ├─ resusableMixinA.js
│   └─ resusableMixinA.spec.js
├── modules
│   ├─ resusableModuleA.js
│   └─ resusableModuleA.spec.js
├── routes
│   └─ index.js
├── store
│   ├─ index.js
│   └─ modules
│       └─ exampleStoreModule
│           ├─ index.js
│           ├─ getters.js
│           ├─ getters.spec.js
│           ├─ mutations.js
│           ├─ mutations.spec.js
│           ├─ actions.js
│           ├─ actions.spec.js
│  		    ├─ mocks
│  		    │   └─ index.js
│  		    └─ api
│  		        └─ index.js
├── utils
│   ├─ index.js
│   └─ utility-a.js
├── views
│   └─ namespaceA
│       ├─ index.js
│       └─ namespaceSectionA
│           ├─ index.js
│           ├─ namespaceSectionA.vue
│  		    └─ namespaceSectionA.spec.js
├── main.js
├── App.vue

```


### Directories Explained

**Assets Directory**

The `assets` directory contains un-compiled assets such as Less, Sass or JavaScript.

**Components Directory**

The `components` directory contains all reusable Vue.js Components.

**Lang Directory**

The `lang` directory contains application i18n translations and language settings.

**Mixins Directory**

The `mixins` directory contains reusable mixins for reusable components and view components.

**Router Directory**

The `router` directory contains application routes.

**Store Directory**

The `store` directory contains all Vuex Store files and modules.

**Utils Directory**

The `utils` directory contains application-wide utilities

**Views Directory**

The `views` directory contains application views and routes.

---

### References
* https://github.com/johnpapa/angular-styleguide/tree/master/a1#application-structure
* https://nuxtjs.org/guide/directory-structure#directories
* https://github.com/igeligel/vuex-namespaced-module-structure
* https://github.com/igeligel/vuex-feature-scoped-structure
* https://hackernoon.com/tips-on-react-for-large-scale-projects-3f9ece85983d