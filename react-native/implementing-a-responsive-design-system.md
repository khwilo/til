# Implementing a responsive design system to React Native

The dimensions we give to each view in React Native are translated to platform specific units:

- Android - **Density pixels**
- iOS - **point**

To achieve responsive design in React Native, utilize the [react-native-responsive-screen](https://github.com/marudy/react-native-responsive-screen) package. This package allows us to specify dimensions as percentages.

```js
import {Text, View} from 'react-native';
import {
  widthPercentageToDP as wp,
  heightPercentageToDP as hp}
from 'react-native-responsive-screen';

const App = () => {
  return (
    <View>
      <View style={styles.textWrapper}>
        <Text>App</Text>
      </View>
    </View>
  )
}

const styles = StyleSheet.create({
  textWrapper: {
    height: hp('50%'),
    width: wp('60%'),
  }
});
```

## References

1. [Implementing a responsive design system to React Native](https://uxdesign.cc/implementing-responsive-design-system-to-react-native-238c0cb7503e)
2. [react-native-responsive-screen](https://github.com/marudy/react-native-responsive-screen)
3. [Build responsive React Native views for any device and support orientation change](https://medium.com/react-native-training/build-responsive-react-native-views-for-any-device-and-support-orientation-change-1c8beba5bc23)
