# Gatsby, next.js, and other JS Frame


### Questions

1. What does React Native do when it builds your application?
- In a nutshell, React Native allows you to build mobile applications that look, feel and perform much more like native applications. It uses the same fundamental UI building blocks as regular iOS and Android apps. You just put those building blocks together using JavaScript and React. React Native is an open-source framework that allows you to build a mobile app with only JavaScript. ... They don't differ from apps built on Java, Objective-C or Swift and they use the same UI building blocks as native iOS or Android apps. But with React Native, building a mobile app is much faster and less expensive

2. Can you simply deploy a react web app to the phone?
- If you’ve used something like create-react-app to bootstrap your project, you’ll want to turn off the built-in service worker if you haven’t specifically integrated it to work with your app. While usually harmless, it can cause some issues, so it’s best to just get rid of it up front.
   - With the key in place, we can finally create our Droplet. To get started, click Create Droplet. You’ll be asked to choose an OS, but for our purposes, the default Ubuntu will work just fine.

You’ll need to select which size Droplet you want to use. In many cases, the smallest Droplet will do. However, review the available options and choose the one that will work best for your project.

Next, select a data center for your Droplet. Choose a location central to your expected visitor base. New features are rolled out by DigitalOcean in different data centers at different times, but unless you know you want to use a special feature that’s only available in specific locations, this won’t matter.

### Terms
| **Term** | **Definition** |
| -- | -- |
| **eject** | Ejecting lets you customize anything, but from that point on you have to maintain the configuration and scripts yourself. This can be daunting if you have many similar projects. In such cases instead of ejecting we recommend to fork react-scripts and any other packages you need. |
| **android avd** | is a configuration that defines the characteristics of an Android phone, tablet, Wear OS, Android TV, or Automotive OS device that you want to simulate in the Android Emulator. The AVD Manager is an interface you can launch from Android Studio that helps you create and manage AVDs |
| **expo** | is a toolchain built around React Native to help you quickly start an app. It provides a set of tools that simplify the development and testing of React Native app and arms you with the components of users interface and services that are usually available in third-party native React Native components. |
