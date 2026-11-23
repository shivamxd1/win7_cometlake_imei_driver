Bringing Intel Comet Lake MEI compatibility to Windows 7.

## Installation

**Requirements**
- Windows 7 SP1 64-bit
- Intel MEI device with hardware ID `PCI\VEN_8086&DEV_06E0`
- Extracted driver package

**Steps**

1. Download `MEI_Win7_06E0_Test.zip` from the repository.
2. Extract the ZIP file to a folder.
3. Open **Device Manager**.
4. Locate the Intel Management Engine Interface device. It may appear under **Other devices** if no compatible driver is installed.
5. Right-click the device and select **Update Driver Software**.
6. Select **Browse my computer for driver software**.
7. Choose **Let me pick from a list of device drivers on my computer**.
8. Click **Have Disk**, then browse to the extracted folder and select `heci.inf`.
9. Follow the prompts to install the driver.
10. Restart Windows if prompted.

**Important Notes**
- This is an experimental INF modification of Intel's original Windows 7 MEI driver version `1914.12.0.1256`.
- The original `TeeDriverx64.sys` binary is unchanged.
- The modified INF does not retain Intel's original catalog signature. Windows may display a driver signature warning or refuse installation.
- If necessary, use Windows 7's Advanced Boot Options (`F8`) and select **Disable Driver Signature Enforcement** for that boot session.
- Tested on Intel Core i3-10105F with an ASRock H470M-HDV motherboard.
- Compatibility with other hardware configurations is not guaranteed.
