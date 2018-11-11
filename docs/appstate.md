---
id: appstate
title: AppState
---

`AppState` может сказать вам, находится ли приложение на переднем плане или в фоновом режиме, и сообщить вам когда состояние изменилось.

AppState часто используется для определения  intent("намерение" - термин и категоря в андроид) и правильное поведение при обработке push-уведомлений.

### App States

* `active` - Приложение работает на переднем плане
* `background` - Приложение работает в фоновом режиме. Пользователь либо:
  * в другом приложении
  * на домашнем экране
  * [Android] на другом `Activity` (даже если он был запущен вашим приложением)
* `inactive` - Это состояние, которое возникает при переходе между фоном и фоном, а также во время периодов бездействия, таких как ввод многозадачного представления или в случае входящего вызова

For more information, see [Apple's documentation](https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/TheAppLifeCycle/TheAppLifeCycle.html)

### Basic Usage

Чтобы увидеть текущее состояние, вы можете проверить `AppState.currentState`, который будет постоянно обновляться. However, `currentState` при запуске будет пустым `AppState` извлекает его через мост.

```
import React, {Component} from 'react'
import {AppState, Text} from 'react-native'

class AppStateExample extends Component {

  state = {
    appState: AppState.currentState
  }

  componentDidMount() {
    AppState.addEventListener('change', this._handleAppStateChange);
  }

  componentWillUnmount() {
    AppState.removeEventListener('change', this._handleAppStateChange);
  }

  _handleAppStateChange = (nextAppState) => {
    if (this.state.appState.match(/inactive|background/) && nextAppState === 'active') {
      console.log('App has come to the foreground!')
    }
    this.setState({appState: nextAppState});
  }

  render() {
    return (
      <Text>Current state is: {this.state.appState}</Text>
    );
  }

}
```

This example will only ever appear to say "Current state is: active" because the app is only visible to the user when in the `active` state, and the null state will happen only momentarily.

### Methods

* [`addEventListener`](appstate.md#addeventlistener)
* [`removeEventListener`](appstate.md#removeeventlistener)

### Properties

* [`currentState`](appstate.md#currentState)

---

# Reference

## Methods

### `addEventListener()`

```javascript
addEventListener(type, handler);
```

Add a handler to AppState changes by listening to the `change` event type and providing the handler

TODO: now that AppState is a subclass of NativeEventEmitter, we could deprecate `addEventListener` and `removeEventListener` and just use `addListener` and `listener.remove()` directly. That will be a breaking change though, as both the method and event names are different (addListener events are currently required to be globally unique).

---

### `removeEventListener()`

```javascript
removeEventListener(type, handler);
```

Remove a handler by passing the `change` event type and the handler

## Properties

### `currentState`

```javascript
AppState.currentState;
```
