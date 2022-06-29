# websocket-to-gamepad
[![Windows](https://svgshare.com/i/ZhY.svg)](https://svgshare.com/i/ZhY.svg)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Repository to map websocket input to virtual gamepad (USB HID-device). Only compatible with Windows.
The emulated gamepad will try to connect to a websocket server and use gamepad input data sent from the server
as values set to the emulated gamepad. 


### Install

For local development, please fork the repository. Then, clone and install in the repository root folder:

```
git clone https://github.com/equinor/websocket-to-gamepad
cd websocket-to-gamepad
pip install -e .
```

### Running websocket-to-gamepad
Specify `host` and `port` configuration variables according to your websocket server:

```bash
WS_SERVER_HOST = 'localhost'
WS_SERVER_PORT = 8000
```

### Testing
To test functionality of your emulated gamepad run [gamepad_tester.py](https://github.com/equinor/websocket-to-gamepad/test/gamepad_tester.py) with a physical gamepad connected and check result on 
[gamepadviewer](https://gamepadviewer.com/). The left joystick should be inverted on the emulated gamepad for the test.