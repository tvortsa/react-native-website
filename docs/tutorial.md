---
id: tutorial
title: Learn the Basics
---

React Native похож на React, но использует в качестве строительных блоков нативные компоненты вместо web компонентов. Для понимания базовой структуры приложения React Native, вы должны понимать некоторые базовые концепции React, такие как JSX, компоненты, `состояния`, и `props`. Если вы уже знакомы с React, вам все равно нужно изучить некоторые React-Native-specific вещи, такие как native components. Этот туториал расчитан на широкую аудиторию вне зависимости знакомы вы с React или нет.

Давайте сделаем это.

## Hello World

В соответствии с древними традициями наших людей мы должны сначала создать приложение, которое ничего не делает, кроме как сказать «Hello world»:

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { Text, View } from 'react-native';

export default class HelloWorldApp extends Component {
  render() {
    return (
      <View>
        <Text>Hello world!</Text>
      </View>
    );
  }
}
```

Если вам интересно, вы можете поиграть с образцом кода прямо в веб-симуляторах. Вы также можете вставить его в свой файл `App.js`, чтобы создать реальное приложение на вашей локальной машине.

## Что тут происходитe?

Некоторые из вещей здесь могут не выглядеть для вас как JavaScript. Но без паники. _This is the future_.

Прежде всего, ES2015 (aтакже известный как ES6) это набор расширений JavaScript который теперь является частью официального стандарта, но еще не поддерживается всеми браузерами, поэтому он часто не используется в веб-разработке. React Native имеет встроенную поддержку ES2015.
`import`, `from`, `class`, и `extends` в примере выше это все возможности ES2015. If you aren't familiar with ES2015, you can probably pick it up just by reading through sample code like this tutorial has. If you want, [this page](https://babeljs.io/learn-es2015/) has a good overview of ES2015 features.

Другая необычная вещь в этом примере кода это `<View><Text>Hello world!</Text></View>`. Это синтаксис JSX - для в XML со встроенным JavaScript. Многие фреймворки используют специальный язык шаблонов, который позволяет вставлять код в язык разметки. В React, наоборот. JSX позволяет писать язык разметки внутри кода. Это похоже на HTML для web, но вместо некоторых web вещей типа `<div>` или `<span>`, you используете React компоненты. В данном случае, `<Text>` это встроенный компонент just displays some text and `View` is like the `<div>` or `<span>`.

## Components

So this code is defining `HelloWorldApp`, a new `Component`. When you're building a React Native app, you'll be making new components a lot. Anything you see on the screen is some sort of component. A component can be pretty simple - the only thing that's required is a `render` function which returns some JSX to render.

## This app doesn't do very much

Good point. To make components do more interesting things, you need to [learn about Props](props.md).
