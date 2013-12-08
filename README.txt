audio_hdmi_hd4000
============
OS X AMD/Nvidia/HD4000 HDMI Audio dsdt edits

This guide enables OS X HDMI audio on Intel based motherboards with a bootable clean install of OS X.  Supported HDMI audio graphics systems are AMD discrete graphics cards (HD5xxx, HD6xxx and HD7xxx), Nvidia discrete graphics cards (4xx, 5xx, 6xx and 7xx) and Intel HD4000 integrated graphics systems.  The Optimized AppleHDA.kext supports HDMI audio and Realtek audio codecs (ALC885, ALC887, ALC888, ALC889, ALC892 and ALC898) for onboard audio.  The native ML AppleHDA.kext supports only HDMI audio when configured properly. In Mountain Lion, the Optimized AppleHDA.kext supports 2 Audio_IDs for HDMI and Realtek onboard audio:
Audio_ID: 1 supports AMD/Nvidia HDMI and 3, 5 and 6 port ALC8xx onboard audio  
Audio_ID: 3 supports HD3000/HD4000 HDMI and 3, 5 and 6 port ALC8xx onboard audio

Note
1. Native AppleHDA.kext, use Audio_ID: 1, for HDMI audio/no onboard audio
2. Integrated and Discrete HDMI audio, use Audio_ID:3, for HDMI audio and Realtek on board audio

OS X versions supported
1. Mavericks.10.9 and newer
2. Mountain Lion/10.8.2 and newer

Location.aml - dsdt.aml/ssdt.aml installation folder
1. Chameleon/Chimera - Extra/
2. Clover - EFI/Clover/ACPI/Patched/

Two HD4000 HDMI audio enabling techniques - select one
1. DSDT - HD4000 HDMI Audio (with dsdt edits) 
2. SSDT - HD4000 HDMI Audio (with native dsdt)

DSDT - HD4000 HDMI Audio
1. MaciASL - http://sourceforge.net/projects/maciasl/?source=navbar
2. Configuration: MaciASL/Preferences/Sources/+/  (copy/paste URL, don't click)
3. URL: https://raw.github.com/toleda/audio_udio_hd400/master
4. Download/ZIP: https://github.com/toleda/audio_hdmi_hd4000

Usage
1. If no dsdt; extract dsdt, MaciASL/File/New from ACPI/DSDT
2. MaciASL/File/Open dsdt
3. MaciASL/Patch/toleda_hdmi_hd4000/Select Patch/es
4. MaciASL/Patch/Apply (Repeat, as necessary) 
5. MaciASL/Patch/Close
6. MaciASL/Compile
7. MaciASL/File/Save As…/ACPI Machine Language Binary/dsdt.aml

Installation - edited dsdt.aml to Extra
1. MaciASL/File/Save As…/ACPI Machine Language Binary/Location.aml/dsdt.aml (add extension)

SSDT - HD4000 HDMI Audio
1. https://github.com/toleda/audio_hdmi_uefi/tree/master/ssdt_7series

Problem Reporting
1. Motherboard/BIOS version/processor/graphics/OS and version
2. Copy of dsdt (if edited)
3. Copy of HDMI audio SSDT (if installed)
4. Copy of IORegistryExplorer

Troubleshooting/Post w/attachments 2-4, above
1. Mavericks/10.9
1a. http://www.tonymacx86.com/hdmi-audio/112469-mavericks-hdmi-audio-applehda.html
1b. http://www.insanelymac.com/forum/topic/292999-mavericks-applehda-hdmi-audio/
2. Mountain Lion/10.8
2a.http://www.tonymacx86.com/hdmi-audio/70762-mountain-lion-hdmi-audio-ami-dsdt.html
2b. http://www.insanelymac.com/forum/topic/291103-mountain-lion-hdmi-audio/

Guides:
1. HD4000/Ivy Bridge/3rd Generation Core Processors/7 Series motherboards/AMI EFI
1a. [Guide] HD4000-hdmi_audio_dsdt_edits_v1.3.pdf.zip
1b. Patches
    IB1. AMI-EFI/Clean Compile - fix native dsdt compiler errors for successful dsdt edits
    IB2. AMI-AMD-Nvidia-7_Series-A1 - AMD/Nvidia HDMI audio dsdt edits
    IB3. AMI-HD4000-7_Series-A3 - HD4000 HDMI audio dsdt edits
    IB4. HD4000-on-6_Series_MB - HD4000 MEI dsdt edit (apply once, only with IB2 or IB3)
    IB5. Award-HD4000-AMD-Nvidia-6_Series-A1 - HD4000/AMD/Nvidia HDMI audio dsdt edits
    IB6. AMI-HD4000-Laptop-FB-01-A3 - Laptop HD4000 HDMI audio dsdt edits
    IB7. AMI-HD4000-Laptop-FB-03-A3 - Laptop HD4000 HDMI audio dsdt edits
    IB8. Intel-HD4000-NUC-A1 - NUC HDMI audio edits (2xHDMI and TB)

toleda
https://github.com/toleda/audio_hdmi_hd4000
Patches
README.txt