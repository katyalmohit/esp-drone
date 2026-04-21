## Steps to flash the chip (ESP-32 SEEED XIAO S3)

### 1. Clone the repository

```bash
git clone https://github.com/katyalmohit/esp-drone.git
```

### 2. Clone ESP-IDF v5.0.7

Clone the official ESP-IDF repository (version 5.0.7) into the project:

```bash
git clone -b v5.0.7 --recursive https://github.com/espressif/esp-idf.git esp-idf-v5.0.7
```

### 3. Navigate to the ESP-IDF directory

```bash
cd esp-idf-v5.0.7/
```

### 4. Install ESP-IDF (first time only)

```bash
./install.sh
```

### 5. Export the ESP-IDF environment

```bash
. ./export.sh
```

> **Note:** You'll need to run `. ./export.sh` in every new terminal session before using `idf.py`.

### 6. Navigate to the firmware directory

```bash
cd ../esp-drone-code/Firmware/esp-drone/
```

### 7. Build the firmware

```bash
idf.py build
```

### 8. (Optional) Access menuconfig

To configure project settings:

```bash
idf.py menuconfig
```

> **Note:** If any changes are made in menuconfig, rebuild the firmware:
>
> ```bash
> idf.py build
> ```

### 9. Flash the firmware

Replace `PORT` with your device's port (e.g., `/dev/ttyUSB0` on Linux, `COM3` on Windows):

```bash
idf.py -p PORT flash
```
