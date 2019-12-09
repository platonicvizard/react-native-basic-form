# React Native Basic Form
React Native Components

### Installation

```bash
$
```

### Form
Shows a form

```javascript
import React from 'react';
import {View} from 'react-native';
import Form, {CTA} from "../../components/react-native-basic-form/index";

export default function Example(props) {
    const [loading, setLoading] = useState(false);

    const fields = [
        {name: 'email', label: 'Email Address', required: true},
        {name: 'password', label: 'Password', required: true, secure: true}
    ];

    async function onSubmit(data) {
        setLoading(true);

        console.log(data)
        ....
    }

    render() {
        return (
            <View>
                <Form
                    title={"Login"} //this is the button title
                    fields={fields}
                    onSubmit={onSubmit}
                    loading={loading}/>
            </View>
        );
    };
};
```

| prop | value | required/optional | description | | description |
| ---- | ----- | ----------------- | ----------- | | ----------- |
| title | string | optional | The button title | "Submit" |
| fields | object | required | the fields to show | [] |
| onSubmit | function | required | the function to call when the submit button is pressed | null |
| loading | boolean | optional | if true, button is disabled and shows a loading icon | false |
| style | function | optional | the style for the container | {{}} |
| keyboardShouldPersistTaps | number | optional | Determines when the keyboard should stay visible after a tap.| 'handled' |

keyboardShouldPersistTaps:https://facebook.github.io/react-native/docs/scrollview#keyboardshouldpersisttaps