# Vue Simple Toggle (Switch)

A simple and super light Vue.js component for simple toggle burtton (switch)

No dependencies. No sass/less compilation. Very easy to use :).

[Static image demo](https://drive.google.com/file/d/0BwXZXJf4wVh0cXhHZXVkV3Z2V28/view?usp=sharing)

## Installation

```bash
npm install vue-libs-simple-toggle --save
```

## Basic Usage

```javascript
import Toggle from 'vue-libs-simple-toggle';

new Vue({

    components: {
        Toggle
    },

    data () {
        return {
            currentState: true
        }
    }
};
```

```html

<toggle v-model="currentState"></toggle>

```

## Customization

Override the relevant classes to customize it. For example, to make it blue instead of green:

```css
    .vue-libs-simple-toggle input:checked + .slider {
        background-color: blue;
    }
    .vue-libs-simple-toggle input:focus + .slider {
        box-shadow: 0 0 1px blue;
    }
```
