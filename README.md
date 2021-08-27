# vue3-code-input

🎉A verification code input compatible with Vue 3.

This is an extension of the npm package by [suweya](https://github.com/suweya) found on [GitHub](https://github.com/suweya/vue-verification-code-input). This package is compatible with Vue 3. This package has been created due to a migration update I was working on from Vue 2 to Vue 3 on a hefty project which used this dependency. This fix is now implemented through this source.

Same implementation as Suweya's Vue 2 version applies - provided below for reference.

## Live demo (thanks to Suweya)

- [Demo](https://suweya.github.io/vue-verification-code-input/index.html)

## Install

```bash
npm install --save vue3-code-input
```

## Usage

```jsx
<template>
  <div id="app">
    <CodeInput :loading="false" class="input" v-on:change="onChange" v-on:complete="onComplete" />
  </div>
</template>

<script>
import CodeInput from "vue3-code-input";

export default {
  name: "app",
  components: {
    CodeInput
  },
  methods: {
    onChange(v) {
      console.log("onChange ", v);
    },
    onComplete(v) {
      console.log("onComplete ", v);
    }
  }
};
</script>
```

## PropTypes

|     Key     |  Type  |              Desc               |
| :---------: | :----: | :-----------------------------: |
|    type     |  text  |      one of number or text      |
|   fields    | number |     The count of characters     |
|  onChange   |  func  |   Trigger on character change   |
| onComplete  |  func  | Trigger on all character inputs |
| fieldWidth  | number |           input width           |
| fieldHeight | number |          input height           |
|  autoFocus  |  bool  | auto focus first input on init  |
|    title    | string |        code input title         |
|   loading   |  bool  |        show loading flag        |
|  className  | string |           class name            |
|   values    | array  |         default values          |

## License

Thanks [suweya](https://github.com/suweya) for the Vue 2 implementation. Credits go to him.
Upgraded by [drewcauchi77](https://github.com/drewcauchi77) for a compatible Vue 3 implementation.