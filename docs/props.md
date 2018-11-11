---
id: props
title: Props
---

Большинство компонентов можно настроить, при создании, разными параметрами. Эти параметры создания называют `props`.

Например, один из основных компонентов React Native - `Image`. Когда вы создаете image, вы можете использовать prop `source` для управления тем како изображение отображать.

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, Image } from 'react-native';

export default class Bananas extends Component {
  render() {
    let pic = {
      uri: 'https://upload.wikimedia.org/wikipedia/commons/d/de/Bananavarieties.jpg'
    };
    return (
      <Image source={pic} style={{width: 193, height: 110}}/>
    );
  }
}

// пропустите эту строку, если используете Create React Native App
AppRegistry.registerComponent('AwesomeProject', () => Bananas);
```

Обратите внимание на скобки, окружающие `{pic}` - они вставляют переменную `pic` в JSX. Вы можете поместить любое выражение JavaScript внутри таких скобок в JSX.

Ваши собственные компоненты также могут использовать `props`. Это позволяет вам создавать один компонент, который используется во многих разных местах вашего приложения, с немного разными свойствами в каждом месте. Просто обратитесь к `this.props` в вашей функции `render`. Пример:

```ReactNativeWebPlayer
import React, { Component } from 'react';
import { AppRegistry, Text, View } from 'react-native';

class Greeting extends Component {
  render() {
    return (
      <View style={{alignItems: 'center'}}>
        <Text>Hello {this.props.name}!</Text>
      </View>
    );
  }
}

export default class LotsOfGreetings extends Component {
  render() {
    return (
      <View style={{alignItems: 'center'}}>
        <Greeting name='Rexxar' />
        <Greeting name='Jaina' />
        <Greeting name='Valeera' />
      </View>
    );
  }
}

// пропустите эту строку, если используете Create React Native App
AppRegistry.registerComponent('AwesomeProject', () => LotsOfGreetings);
```

Используйте `name` как prop который позволяет нам изменять компонент `Greeting`, поэтому мы можем повторно использовать этот компонент для каждого из наших приветствий. В этом примере также используется компонент `Greeting` в JSX, как встроенные компоненты. Это то что делает React таким крутым - если вы захотите, чтобы у вас был другой набор UI примитивов, вы просто изобретаете новые.

Другое новое, что происходит здесь, - это компонент [`View`](view.md).  [`View`](view.md) удобен как контейнер для других компонентов, помогающий управлять стилями и расположением.

С `props` и базовыми компонентами [`Text`](text.md), [`Image`](image.md), и [`View`](view.md) , выможете построить широкий спектр статических экранов. Чтобы узнать, как изменить свое приложение со временем, вам необходимо [изучить State](state.md).
