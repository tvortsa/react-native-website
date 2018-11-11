---
id: components-and-apis
title: Components and APIs
---

React Native предоставляет ряд встроенных компонентов. Вы найдете полный список компонентов и API на сайдбаре слева. Если вы не знаете, с чего начать, ознакомьтесь со следующими категориями::

* [Базовые компоненты](components-and-apis.md#basic-components)
* [Интерфейс пользователя](components-and-apis.md#user-interface)
* [Списки](components-and-apis.md#list-views)
* [iOS-специфические](components-and-apis.md#ios-components-and-apis)
* [Android-специфические](components-and-apis.md#android-components-and-apis)
* [Другие](components-and-apis.md#others)

Вы не ограничены компонентами и API поставляемыми с React Native. React Native это сообщество тысяч разработчиков. Если вы ищете библиотеку, которая делает что-то конкретное, выполните поиск в реестре npm для упомянутых пакетов [react-native](https://www.npmjs.com/search?q=react-native&page=1&ranking=optimal), или [Awesome React Native](http://www.awesome-react-native.com/) курируемый список.

## Базовые компоненты

Большинство приложений в конечном итоге будут использовать один из этих базовых компонентов. Вы захотите ознакомиться с ними, если вы новичок в React Native.

<div class="component-grid component-grid-border">
  <div class="component">
    <h3><a href="view.html">View</a></h3>
    <p>Самый фундаментальный компонент для создания пользовательского интерфейса.</p>
  </div>
  <div class="component">
    <h3><a href="text.html">Text</a></h3>
    <p>Компонент для отображения текста.</p>
  </div>
  <div class="component">
    <h3><a href="image.html">Image</a></h3>
    <p>Компонент для отображения изображений.</p>
  </div>
  <div class="component">
    <h3><a href="textinput.html">TextInput</a></h3>
    <p>Компонент для ввода текста в приложение с помощью клавиатуры.</p>
  </div>
  <div class="component">
    <h3><a href="scrollview.html">ScrollView</a></h3>
    <p>Предоставляет прокручивающийся контейнер, в котором могут размещаться несколько компонентов и представлений..</p>
  </div>
  <div class="component">
    <h3><a href="stylesheet.html">StyleSheet</a></h3>
    <p>Обеспечивает уровень абстракции, аналогичный стилям CSS.</p>
  </div>
</div>

## Пользовательский интерфейс

Рендер общих элементов управления пользовательского интерфейса на любой платформе, используя следующие компоненты. Для конкретных компонентов платформы продолжайте чтение.

<div class="component-grid component-grid-border">
  <div class="component">
    <h3><a href="button.html">Button</a></h3>
    <p>Основной компонент кнопки для обработки жестов, который должен хорошо отображаться на любой платформе.</p>
  </div>
  <div class="component">
    <h3><a href="picker.html">Picker</a></h3>
    <p>Renders the native picker component на iOS и Android.</p>
  </div>
  <div class="component">
    <h3><a href="slider.html">Slider</a></h3>
    <p>Компонент, используемый для выбора одного значения из диапазона значений.</p>
  </div>
  <div class="component">
    <h3><a href="switch.html">Switch</a></h3>
    <p>Renders a boolean input.</p>
  </div>
</div>

## List Views

В отличие от более общего `ScrollView`, этот компонент списка рендерит только те компоненты которые в данный момент отображены на экране. Это делает их отличным выбором для отображения длинных списков данных.

<div class="component-grid component-grid-border">
  <div class="component">
    <h3><a href="flatlist.html">FlatList</a></h3>
    <p>Компонент для рендеринга прокручиваемых списков.</p>
  </div>
  <div class="component">
    <h3><a href="sectionlist.html">SectionList</a></h3>
    <p>Like <code>FlatList</code>, но для секционных списков.</p>
  </div>
</div>

## iOS Components and APIs

Many of the following components provide wrappers for commonly used UIKit classes.

<div class="component-grid component-grid-border">
  <div class="component">
    <h3><a href="actionsheetios.html">ActionSheetIOS</a></h3>
    <p>API to display an iOS action sheet or share sheet.</p>
  </div>
  <div class="component">
    <h3><a href="alertios.html">AlertIOS</a></h3>
    <p>Create an iOS alert dialog with a message or create a prompt for user input.</p>
  </div>
  <div class="component">
    <h3><a href="datepickerios.html">DatePickerIOS</a></h3>
    <p>Renders a date/time picker (selector) on iOS.</p>
  </div>
  <div class="component">
    <h3><a href="imagepickerios.html">ImagePickerIOS</a></h3>
    <p>Renders a image picker on iOS.</p>
  </div>
  <div class="component">
    <h3><a href="navigatorios.html">NavigatorIOS</a></h3>
    <p>A wrapper around <code>UINavigationController</code>, enabling you to implement a navigation stack.</p>
  </div>
  <div class="component">
    <h3><a href="progressviewios.html">ProgressViewIOS</a></h3>
    <p>Renders a <code>UIProgressView</a></code> on iOS.</p>
  </div>
  <div class="component">
    <h3><a href="pushnotificationios.html">PushNotificationIOS</a></h3>
    <p>Handle push notifications for your app, including permission handling and icon badge number.</p>
  </div>
  <div class="component">
    <h3><a href="segmentedcontrolios.html">SegmentedControlIOS</a></h3>
    <p>Renders a <code>UISegmentedControl</code> on iOS.</p>
  </div>
  <div class="component">
    <h3><a href="tabbarios.html">TabBarIOS</a></h3>
    <p>Renders a <code>UITabViewController</code> on iOS. Use with <a href="tabbarios-item.html">TabBarIOS.Item</a>.</p>
  </div>
</div>

## Android Components and APIs

Многие из следующих компонентов предоставляют обертки для обычно используемых классов Android.

<div class="component-grid component-grid-border">
  <div class="component">
    <h3><a href="backhandler.html">BackHandler</a></h3>
    <p>Обнаружение аппаратных нажатий кнопок для обратной навигации.</p>
  </div>
  <div class="component">
    <h3><a href="datepickerandroid.html">DatePickerAndroid</a></h3>
    <p>Открывает стандартный Android диалог выбора даты.</p>
  </div>
  <div class="component">
    <h3><a href="drawerlayoutandroid.html">DrawerLayoutAndroid</a></h3>
    <p>Рендерит андроидовский <code>DrawerLayout</code>.</p>
  </div>
  <div class="component">
    <h3><a href="permissionsandroid.html">PermissionsAndroid</a></h3>
    <p>Предоставляет доступ к модели разрешений, представленной в Android M.</p>
  </div>
  <div class="component">
    <h3><a href="progressbarandroid.html">ProgressBarAndroid</a></h3>
    <p>Renders a <code>ProgressBar</code> on Android.</p>
  </div>
  <div class="component">
    <h3><a href="timepickerandroid.html">TimePickerAndroid</a></h3>
    <p>Opens the standard Android time picker dialog.</p>
  </div>
  <div class="component">
    <h3><a href="toastandroid.html">ToastAndroid</a></h3>
    <p>Create an Android Toast alert.</p>
  </div>
  <div class="component">
    <h3><a href="toolbarandroid.html">ToolbarAndroid</a></h3>
    <p>Renders a <code>Toolbar</code> on Android.</p>
  </div>
  <div class="component">
    <h3><a href="viewpagerandroid.html">ViewPagerAndroid</a></h3>
    <p>Контейнер, который позволяет перевернуть влево и вправо между дочерними представлениями.</p>
  </div>
</div>

## Другие

Эти компоненты могут пригодиться для определенных приложений. Для исчерпывающего списка компонентов и API-интерфейсов проверьте боковую панель слева.

<div class="component-grid">
  <div class="component">
    <h3><a href="activityindicator.html">ActivityIndicator</a></h3>
    <p>Отображает круговой индикатор загрузки.</p>
  </div>
  <div class="component">
    <h3><a href="alert.html">Alert</a></h3>
    <p>Запускает диалоговое окно предупреждения с указанным заголовком и сообщением</p>
  </div>
  <div class="component">
    <h3><a href="animated.html">Animated</a></h3>
    <p>Библиотека для создания жидких, мощных анимаций, которые легко создавать и поддерживать.</p>
  </div>
  <div class="component">
    <h3><a href="cameraroll.html">CameraRoll</a></h3>
    <p>Обеспечивает доступ к локальной камере / галерее.</p>
  </div>
  <div class="component">
    <h3><a href="clipboard.html">Clipboard</a></h3>
    <p>Предоставляет интерфейс для настройки и получения содержимого из буфера обмена в iOS и Android.</p>
  </div>
  <div class="component">
    <h3><a href="dimensions.html">Dimensions</a></h3>
    <p>Обеспечивает интерфейс для получения размеров устройства.</p>
  </div>
  <div class="component">
    <h3><a href="keyboardavoidingview.html">KeyboardAvoidingView</a></h3>
    <p>Предоставляет представление, которое автоматически перемещается из виртуальной клавиатуры.</p>
  </div>
  <div class="component">
    <h3><a href="linking.html">Linking</a></h3>
    <p>Предоставляет общий интерфейс для взаимодействия с входящими и исходящими ссылками на приложения.</p>
  </div>
  <div class="component">
    <h3><a href="modal.html">Modal</a></h3>
    <p>Предоставляет простой способ представления содержимого над закрытым представлением.</p>
  </div>
  <div class="component">
    <h3><a href="pixelratio.html">PixelRatio</a></h3>
    <p>Обеспечивает доступ к плотности пикселей устройства.</p>
  </div>
  <div class="component">
    <h3><a href="refreshcontrol.html">RefreshControl</a></h3>
    <p>Этот компонент используется внутри <code>ScrollView</code> для добавления функционала обновления.</p>
  </div>
  <div class="component">
    <h3><a href="statusbar.html">StatusBar</a></h3>
    <p>Компонент для управления панелью состояния приложения.</p>
  </div>
  <div class="component">
    <h3><a href="webview.html">WebView</a></h3>
    <p>Компонент, который отображает веб-контент в native view.</p>
  </div>
</div>
