# Example - Plugin React Native PushLink

<p align="center">
  <img src="https://pushlink.com/javax.faces.resource/images/site/logo-verde.png.xhtml?ln=pushlink" height='130' />
  </br>
  </br>
</p>

## <a href="https://github.com/diogo-bruno/react-native-push-link">`React Native - PushLink`</a>

---

<p align="center">
<br>
 ScreenShot Example Application
<br><br>
<img src="https://user-images.githubusercontent.com/11491923/110528809-4eaa6780-80f7-11eb-9525-2dbeb93238e5.png" width="350" />
</p>

---

## `Test project`

```sh
git clone https://github.com/diogo-bruno/react-native-push-link-example.git
cd react-native-push-link-example
yarn install
react-native pushlink-prepare-project
yarn start
yarn android
```

## `Usage code example`

```javascript
...
import PushLink from 'react-native-push-link';
...

componentDidMount = () => {

  const deviceId = await PushLink.getDeviceId().catch((e) => e);

  const pushLinkStarted = await PushLink.start(PUSH_LINK_API_KEY, deviceId).catch((e) => e);

};
```

<a target="_blank" href="https://github.com/diogo-bruno/react-native-push-link-example/blob/master/App.js">Open file Application: <b>App.js</b></a>

---
