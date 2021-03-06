# Recoding AMR file to microSD 

The example records 10 seconds AMR-NB or AMR-WB audio file to microSD Card. The AMR audio compression format is optimized for speech coding and produces much smaller output files comparing to other popular codecs.

This demo makes use of callback function instead of Message Queue for events. For instance, [pipeline_amr_sdcard](examples/recorder/pipeline_amr_sdcard) example uses Message Queue for events.

## Compatibility

| ESP32-LyraT | ESP32-LyraTD-MSC | ESP32-LyraT-Mini |
|:-----------:|:---------------:|:----------------:|
| [![alt text](../../../docs/_static/esp32-lyrat-v4.2-side-small.jpg "ESP32-LyraT")](https://docs.espressif.com/projects/esp-adf/en/latest/get-started/get-started-esp32-lyrat.html) | [![alt text](../../../docs/_static/esp32-lyratd-msc-v2.2-small.jpg "ESP32-LyraTD-MSC")](https://docs.espressif.com/projects/esp-adf/en/latest/get-started/get-started-esp32-lyratd-msc.html) | [![alt text](../../../docs/_static/esp32-lyrat-mini-v1.2-small.jpg "ESP32-LyraT-Mini")](https://docs.espressif.com/projects/esp-adf/en/latest/get-started/get-started-esp32-lyrat-mini.html) |
| ![alt text](../../../docs/_static/yes-button.png "Compatible") | ![alt text](../../../docs/_static/yes-button.png "Compatible") | ![alt text](../../../docs/_static/yes-button.png "Compatible") |

## Usage

Prepare the audio board:

- Insert a microSD card into board's slot.

Configure the example:

- Select compatible audio board in `menuconfig` > `Audio HAL`.
- You may change between AMR-NB and AMR-WB encoder in `menuconfig` > `Example configuration` > `Audio encoder file type`. 

Load and run the example:

- Speak to the board once prompted on the serial monitor.
- After finish, you can open `/sdcard/rec.amr` or `/sdcard/rec.Wamr` to hear the recorded file.
