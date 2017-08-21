# Vue Simple Toggle (Switch)

A simple and super light Vue.js component for simple toggle button (switch) with a nice smooth transition.

No dependencies. No sass/less compilation. Very easy to use :).

<img src="https://raw.githubusercontent.com/AlexLibs/vue-libs-simple-toggle/master/demo/vue-libs-simple-toggle-demo.png" /><br>


[How it looks DEMO](https://jsfiddle.net/bqqydhjL/3/show/)

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
        background-color: blue!important;
    }
    .vue-libs-simple-toggle input:focus + .slider {
        box-shadow: 0 0 1px blue!important;
    }
```
