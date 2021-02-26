<p align="center">
  <img src="https://pushlink.com/javax.faces.resource/images/site/logo-verde.png.xhtml?ln=pushlink" height='130' />
  </br>
  </br>
</p>

# `Example - Plugin React Native PushLink`

## `Plugin PushLink - React Native`

<https://github.com/diogo-bruno/react-native-push-link/>

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

  const strategyCustom = await PushLink.setStrategyCustom(
    { TypeBroadcastReceiver: 'APPLY' },
    (responseBroadcast) => {
      console.log(responseBroadcast);
      // new APK for install...

      // Open modal user interaction or silent install...
      const install = await PushLink.installApk().catch((e) => e);
    },
  ).catch((e) => e);

};
```
