# tuya_telegram_bot
This script is an example of a Python program that uses the `telebot` and `tinytuya` libraries to control a Tuya smart plug via a Telegram bot. The script allows the user to send commands to the bot and interact with the Tuya device.

The `telebot` library is used to create a Telegram bot instance and handle incoming commands from users. The `tinytuya` library is used to communicate with the Tuya device and control its state.

The script starts by defining several constants, including the Telegram bot API token, the allowed user IDs, and the Tuya device ID, IP address, and local key. The script also defines several device state constants, such as `DEVICE_STATE_ON` and `DEVICE_STATE_OFF`.

Next, the script creates instances of the `OutletDevice` class from the `tinytuya` library and the `TeleBot` class from the `telebot` library. The `OutletDevice` instance is used to communicate with the Tuya device, while the `TeleBot` instance is used to handle incoming Telegram commands.

The script defines several handler functions, such as `send_welcome`, `run_status`, `run_on`, `run_off`, and `run_timer`, which are triggered by different Telegram commands. These functions check if the user sending the command is allowed to interact with the bot and execute the corresponding action on the Tuya device.

For example, the `run_on` function turns the Tuya device on if it is not already on, while the `run_off` function turns it off if it is not already off. The `run_timer` function sets a timer for the device to turn off after a specified number of minutes.
