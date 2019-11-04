# nodegui-os-utils

A nodegui helper module which will contain OS specific native features which Qt doesnt support and hence requires native code in respective operting systems.

# Installation

```
npm install @nodegui/nodegui-os-utils
```

# Usage

```js
import { Dock } from "@nodegui/os-utils";

console.log("Showing the Dock icon on macOS");
Dock.show();
console.log("Hiding the Dock icon on macOS");
Dock.hide();
```
```js
import { AboutPanel } from "@nodegui/os-utils";

console.log("Open the about panel on macOS");
AboutPanel.open();
console.log("Open the about panel on macOS with modified defaults");
AboutPanel.open({ name: "Custom name", version: "2.3.5" });
```

# Supported APIs

## macOS

- Dock
  - `show()` - static method - Shows the Dock icon on macOS. Does nothing on other platforms.
  - `hide()` - static method - Hides the Dock icon on macOS. Does nothing on other platforms.

- AboutPanel
  - `open(options?: object)` - static method - Opens the about panel on macOS. Does nothing on other platforms. `options` is optional and can contain the following strings: `name`, `version`, `applicationVersion`, and `copyright`. The default values are derived from `Info.plist`.

# License

MIT
