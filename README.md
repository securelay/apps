# apps
This is a registry for apps that use Securelay as backend.

Securelay sends web-push notifications to an app using the registered details. 

To register your app, add `<your-app-name>.json` containing the necessary details and submit a PR to this repository.

### JSON template
The JSON should contain the following keys, some of which are optional. Most take string-typed values.

- `app` : Name of the app
- `webPush` : Specify the web-push notification
    - `ifOrigin` : Optional. Comma-separated list if multiple origins. If provided, Securelay creates a web-push only if the triggering request matches one of the listed origins in its [Origin](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Origin) header.
    - `sendData` : Optional. Boolean. If provided and `true`, Securelay adds the triggering request's body to the web-push as [additional data](https://documentation.onesignal.com/reference/push-notification#custom-data--categories).
    - `title` : Notification header
    - `url` : Clicking the notification would open this link
    - `icon` : URL to app logo or icon
    - `message` : Message to be shown in the notification body

See [formonit.json](./formonit.json) as an example.

### Contact
For any query, feel free to contact us.
- Create an [issue](https://github.com/securelay/apps/issues)
- Email us at [securelay.github.io@gmail.com](mailto:securelay.github.io@gmail.com)
