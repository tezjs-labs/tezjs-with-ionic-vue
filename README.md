## Tezjs with Ionic Vue

- Ionic Vue is An open source mobile UI toolkit for building modern, high-quality cross-platform App.

- We can use Ionic Vue with Tezjs by following steps.

- Make a new tezjs project.

```
npm create tez@latest
```
- Install the latest version of Ionic or run :

```
npm install @ionic/vue
```
- Now add it as a plugin, make a plugins directory, add index.ts inside it, and add the below code.
   **plugins/index.ts**
```
import { IonicVue } from '@ionic/vue';

export default function(vue:any){
    vue.use(IonicVue)
}  
```

- Core CSS  required for Ionic components to work properly 
```
assets/index.css

@import '@ionic/vue/css/core.css';
```

- Basic CSS for apps built with Ionic
```
assets/index.css

import "@ionic/vue/css/normalize.css";
import "@ionic/vue/css/structure.css";
import "@ionic/vue/css/typography.css";    
```

- Optional CSS utils that can be commented out
```
assets/index.css

import '@ionic/vue/css/padding.css';
import '@ionic/vue/css/float-elements.css';
import '@ionic/vue/css/text-alignment.css';
import '@ionic/vue/css/text-transformation.css';
import '@ionic/vue/css/flex-utils.css';
import '@ionic/vue/css/display.css';
```

- It's done with Tezjs. You can now use it in your project.

- In the current project all components and pages are designed with a Ionic framework.

- **Note**: For more information on Ionic Vue, visit : https://ionicframework.com/docs.