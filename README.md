# Bottom drawer for React Native

<p align="center">
  <img src="https://github.com/rationalappdev/react-native-bottom-drawer/blob/master/demo.gif" alt="Demo" width="375" />
</p>

## Content

- [Installation](#installation)
- [Usage example](#usage-example)
- [Configuration](#configuration)
- [Questions?](#questions)

## Installation

#### Step 1

Install [react-native-vector-icons](https://github.com/oblador/react-native-vector-icons#installation) if you do not already have it.

```
npm install react-native-vector-icons --save && react-native link react-native-vector-icons
```

#### Step 2

Install `react-native-bottom-drawer`

```
npm install react-native-bottom-drawer --save
```

## Usage Example

```javascript
import React, { Component } from 'react';
import {
  Image,
  StatusBar,
  StyleSheet,
  View
} from 'react-native';
import Drawer, { Message } from 'react-native-bottom-drawer';

export default class App extends Component {
  render() {
    return (
      <View style={styles.container}>
        <StatusBar barStyle={"light-content"} />
        <Image style={styles.image} source={{uri: 'https://i.imgur.com/Ew8AIQ3.jpg'}}>
          <Drawer>
            <Message
              title="World Agrees To Just Take Down Internet For A While Until They Can Find A Good Use For It"
              message="NEW YORK—Saying the global computer network will cease to be available to users as of midnight tonight, the people of the world announced plans Wednesday to shut down the entire internet until such time as a good use for it can be found. According to the earth’s 7.5 billion inhabitants, the internet—a technology that allows every human on the face of the planet to communicate and share data with every other human—seemed like an excellent idea at first. But while limited parts of the internet were deemed beneficial and may one day be salvaged, the global populace concluded that the overwhelming majority of it is really awful, and in some cases, even dangerous."
            />
            <Message
              title="Middle Eastern Man Not Sure How Many Days’ Worth Of Airport Detention Clothes To Pack"
              message="MUSCAT, OMAN—Sifting through various items in his dresser and closet, 36-year-old Omani graduate student Raed Saleh told reporters Monday that he was not sure how many days’ worth of airport detention clothes to bring for his upcoming trip to the United States. “I definitely want to pack enough to last me the entire time I’m detained at Newark International Airport, but I also don’t want to overdo it,” said Saleh, adding that five T-shirts would likely be enough to avoid having to do laundry while he is being held for questioning by Immigration and Customs Enforcement agents..."
            />
            <Message
              title="DAY 45: Jeff Sessions Spits In Face Of FBI Interrogator Trying To Get Him To Turn On Trump"
              message="WASHINGTON—Angrily dismissing offers of a plea deal if he would agree to cooperate with an investigation into the current administration’s ties to Russia, Attorney General Jeff Sessions reportedly spit in the face of an FBI interrogator Thursday who was attempting to convince him to turn on President Trump. “If you goddamn Feds want to know whether I’ll turn rat: Here’s my answer,” said Sessions, shortly before leaning over the small wooden table separating him and his interrogator and spitting directly into the FBI official’s eyes. “I’m not gonna crack, so you G-men can threaten me with whatever the hell you want—you’re just wasting your time. I’ll fucking die before I flip, so you got the balls to kill me?”"
            />
          </Drawer>
        </Image>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
  },
  image: {
    flex: 1,
  },
});
```

## Configuration

| prop | type | default | description |
| ---- | ---- | ----| ---- |
| children | any | none | Component or components to render inside drawer |
| isOpen | bool | false | Whether the window is open or not | 
| header | string | Messages | Header that shows up on top the screen when opened |
| headerHeight | number | 70 | Header height |
| teaserHeight | number | 75 | Height of the visible teaser area at the bottom of the screen |

### Questions?
Feel free to contact me at [	konstantin.shkut@gmail.com](mailto:konstantin.shkut@gmail.com) or [create an issue](https://github.com/rationalappdev/react-native-bottom-drawer/issues/new)