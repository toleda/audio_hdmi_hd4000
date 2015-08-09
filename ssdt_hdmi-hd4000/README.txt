audio_hdmi_hd4000/ssdt_hdmi-hd4000
============
OS X Ivy Bridge/7 Series/Socket 1155 - HD4000 HDMI Audio ssdt
OS X Ivy Bridge/6 Series/Socket 1155 - HD4000 HDMI Audio ssdt

ssdt_hdmi-hd4000-7series-3
Supports Desktop/HD4000
Injects Capri/framebuffer: 0x0A006601 (DP DP HDMI)
Requires Audio ID: 3

ssdt_hdmi-hd4000-6series-3
Supports Desktop/HD4000
Injects Capri/framebuffer: 0x07006201 (DP DP HDMI)
Injects MEI,  0x3A1E0000
Requires Audio ID: 3

ssdt_hdmi-hd400+_AirPlay
Enables Airplay Mirroring without HD4000 graphics
Injects Capri/framebuffer: 0x04001204 (no connectors)

HD 4000 HDMI audio
OS X/Desktop/HD4000 audio is native, see
[Guide]_HD4000-hdmi_audio_(dsdt_or_ssdt)
https://github.com/toleda/audio_hdmi_hd4000

HD4000 HDMI audio:
1. DP audio is native
2. HDMI audio is native (requires HDMI connector on Capri/Port 0x7)

HD4000 AirPlay Mirroring is native

Installation (included in download)
1. [Guide]-OSX_ssdt-installation

Problem Reporting: see https://github.com/toleda/audio_hdmi_hd4000 README.txt

toleda
https://github.com/toleda/audio_hdmi_hd4000/ssdt_hdmi-hd4000
README.txt