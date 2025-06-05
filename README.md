# <div align='center'>Baileys - Typescript/Javascript WhatsApp Web API</div>

<div align="center"><img src="https://files.catbox.moe/ha98vk.jpg"></div>

## Important Note

The original repository was initially removed by its creator and subsequently taken over by [WhiskeySockets](https://github.com/WhiskeySockets). Building upon this foundation, I have implemented several enhancements and introduced new features that were not present in the original repository. These improvements aim to elevate functionality and provide a more robust and versatile experience.

## Install

Install in package.json:
```json
"dependencies": {
    "baileys": "github:ArdSvt/Baileyslib"
}
```
or install in terminal:
```
npm install baileys@github:ArdSvt/Baileyslib
```

Then import the default function in your code:
```ts 
// type esm
import makeWASocket from 'baileys'
```

```js
// type cjs
const { default: makeWASocket } = require("baileys")
```

## Added Features and Improvements
Here are some of the features and improvements I have added:

- **Support for Sending Messages to Channels**: You can now easily send messages to channels.

- **Support for Button Messages and Interactive Messages**: Added the ability to send messages with buttons and interactive messages.

- **AI Message Icon**: Added customizable AI icon settings for messages

- **Profile Picture Settings**: Allows users to upload profile pictures in their original size without cropping, ensuring better quality and visual presentation.

- **Custom Pairing Code**: Users can now create and customize pairing codes as they wish, enhancing convenience and security when connecting devices.

- **Libsignal Fixes**: Cleaned up logs for a cleaner and more informative output.

More features and improvements will be added in the future.

## Feature Examples

### Custom Code Pairing

```ts
if(usePairingCode && !sock.authState.creds.registered) {
    const phoneNumber = await question('Please enter your mobile phone number:\n')
    const custom = "ARDACRTR" // must be 8 digits, can be letters or numbers
    const code = await sock.requestPairingCode(phoneNumber, custom)
    console.log(`Pairing code: ${code?.match(/.{1,4}/g)?.join('-') || code}`)
}
```

## Reporting Issues
If you encounter any issues while using this repository or any part of it, please feel free to open a [new issue](https://github.com/ArdSvt/Baileyslib/issues) here.

## Notes
Everything other than the modifications mentioned above remains the same as the original repository. You can check out the original repository at [WhiskeySockets](https://github.com/WhiskeySockets/Baileys)