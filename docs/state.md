---
id: state
title: State
---

Существует два типа данных, которые управляют компонентом: `props` и `state`. `props` устанавливаются родителем, и остаются фиксированными на протяжении всего жизненного цикла компонента. Для данных, которые будут меняться, используются `state`.

В общем, вы должны инициализировать `state` в конструкторе, и затем вызывать `setState` когда хотите изменить его.

Например, скажем мы хотим сделать мигающий текст. Сам текст получает один раз при создании мигающего компонента, поэтому сам текст является `prop`. "включен текст или выключен" изменяется со временем, поэтому его следует хранить в `state`.

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, Text, View } from 'react-native';

class Blink extends Component {
  constructor(props) {
    super(props);
    this.state = { isShowingText: true };

    // Переключаем состояние каждую секунду
    setInterval(() => (
      this.setState(previousState => (
        { isShowingText: !previousState.isShowingText }
      ))
    ), 1000);
  }

  render() {
    if (!this.state.isShowingText) {
      return null;
    }

    return (
      <Text>{this.props.text}</Text>
    );
  }
}

export default class BlinkApp extends Component {
  render() {
    return (
      <View>
        <Blink text='I love to blink' />
        <Blink text='Yes blinking is so great' />
        <Blink text='Why did they ever take this out of HTML' />
        <Blink text='Look at me look at me look at me' />
      </View>
    );
  }
}

// skip this line if using Create React Native App
AppRegistry.registerComponent('AwesomeProject', () => BlinkApp);
```

В реальном приложении вы, вероятно, не будете устанавливать состояние с помощью таймера. Вы можете установить состояние, когда у вас появились новые данные с сервера или с пользовательского ввода. Вы также можете использовать контейнер состояния, например [Redux](https://redux.js.org/) или [Mobx](https://mobx.js.org/) для управления потоком данных. В этом случае вы должны использовать Redux или Mobx для изменения своего состояния, а не вызывать `setState` напрямую.

Когда setState вызван, BlinkApp будет перерендеривать этот Component. Вызов setState с Timer, компонент будет перерисовываться каждый раз, когда тикает Таймер.

State работает так же, как и в React, поэтому для получения более подробной информации об управлении состоянием, вы можете посмотреть на [React.Component API](https://reactjs.org/docs/react-component.html#setstate). На данный момент вас может раздражать то, что большинство наших примеров до сих пор используют скучный черный текст по умолчанию. Чтобы сделать вещи более красивыми, вам придется [learn about Style](style.md).
