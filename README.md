## Steps to flash the chip (ESP-32 SEEED XIAO S3)

### 1. Clone the repository

```bash
git clone git@github.com:katyalmohit/esp-drone.git
```

### 2. Navigate to the ESP-IDF directory

```bash
cd esp-drone/esp-idf-v5.0.7/
```

### 3. Export the ESP-IDF environment

```bash
. ./export.sh
```

### 4. Navigate to the firmware directory

```bash
cd ../esp-drone-code/Firmware/esp-drone/
```

### 5. Build the firmware

```bash
idf.py build
```

### 6. (Optional) Access menuconfig

To configure project settings:

```bash
idf.py menuconfig
```

> **Note:** If any changes are made in menuconfig, rebuild the firmware:
>
> ```bash
> idf.py build
> ```

### 7. Flash the firmware

Replace `PORT` with your device's port (e.g., `/dev/ttyUSB0` on Linux, `COM3` on Windows):

```bash
idf.py -p PORT flash
```
