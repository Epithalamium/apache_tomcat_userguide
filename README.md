# AMD Desktop Config

## Jump Install Network Connections Guide < if haven't "Enter Without Net" Option >

when on network selection page > Shift+F10 > input "oobe\BypassNRO.cmd" > Windows will auto restart > "I haven't Internet Connections" > "Continue With Restricted Settings" > u can create local account now

## Basic Settings

### Necessary Drivers

AMD Auto-select Program stand last(need net connection)

### Windows update

### Power Plan

Settings > Power Plan > Ultimate<br>
Settings > Power Plan > Screen and sleep > all check "Never"

### Config (MSI Motherboard)

1.Advanced > Settings > Advanced > PCIe/PCI Subsystem Settings > Re-Size BAR Support -> "enabled" (need mass GPU mem)

2.Advanced > Settings > Security > Trusted Computing > AMD fTPM switch -> "disabled"

3.OC > OC Explore Mode->[Expert] > Advanced CPU Configuration > Kombo Strike->[3] > AMD CBS > Global C-state Control->[disabled] (CPPC and CPPC Preferred Cores can disable for stability,enable for high r23 points)(cppc1-enable;cppc2-disable)

4.OC > CPU Offset Voltage(-)->[0.0625V]

### Set "This PC" as start page

File Explorer > ··· > Options > Opens File Explorer To > check "This PC"<br>
File Explorer > ··· > Options > Privacy > all uncheck

### Download Necessary Applications

#### Page Download

Asus driverhub
[Thorium](https://github.com/Alex313031/Thorium-Win/releases)<br>
[Optimizer](https://github.com/hellzerg/optimizer)<br>
Win11EZToUse<br>
Windows Cursor Enhancement<br>
[图吧工具箱](https://www.tbtool.cn/)<br>

#### 2 download

[Logitech G Hub](https://www.logitechg.com/en-us/innovation/g-hub.html)<br>
[Voicemeeter](https://voicemeeter.com/)<br>
[ContextMenuManager](https://github.com/BluePointLilac/ContextMenuManager)<br>
[qbittorrent](https://www.fosshub.com/qBittorrent.html)<br>
[Steam](https://store.steampowered.com/about/)<br>
[Steam++](https://steampp.net/)<br>
[Telegram](https://apps.microsoft.com/detail/9n97zckpd60q?hl=en-US&gl=US)<br>
[Video Converter](https://handbrake.fr/downloads.php)<br>
[Magpie](https://github.com/Blinue/Magpie?tab=readme-ov-file)<br>
[LockHunter](https://lockhunter.com/download.htm)<br>
[File Shredder](https://www.fileshredder.org/)<br>
[quicklook](https://github.com/QL-Win/QuickLook)<br>
[FanControl](https://github.com/Rem0o/FanControl.Releases)<br>
[AutoDarkMode](https://github.com/AutoDarkMode/Windows-Auto-Night-Mode)<br>
[HiBit Uninstaller](https://www.hibitsoft.ir/Uninstaller.html)<br>
[Animeko](https://myani.org/downloads)<br>
[bilidownloader](https://github.com/LightQuanta/BiliResourceDownloader)<br>
DSX<br>
[Everything](https://everything.en.uptodown.com/windows/download)<br>
[Filerennamer](https://github.com/ilgnefz/once_power)<br>
[Game_Cheats_Manager](https://github.com/dyang886/Game-Cheats-Manager)<br>
[Locale_Emulator](https://github.com/xupefei/Locale-Emulator)<br>
[LocalSend](https://localsend.org/download?os=windows)<br>
[Lossless_Cut](https://github.com/mifi/lossless-cut)<br>
[VScode](https://code.visualstudio.com/download)<br>
[MobaXterm](https://mobaxterm.mobatek.net/download.html)<br>
[慕遜公益](https://mxfree.ao-x.ac.cn/chi/)<br>
[KMplayer](https://www.kmplayer.com/home#layer-64x)<br>
[ScreenToGif](https://www.screentogif.com/)<br>
[SonyMusicCenter](https://www.sony.com.hk/zh/electronics/support/articles/MC4PC020001?srsltid=AfmBOorScW6EVK8K-NBdzipK003hFhN8Kdarr8wzejA9MkZ3wsUMzQRQ)<br>
[Syncthing](https://syncthing.net/downloads/)<br>
[taskbarX](https://taskbarx.org/)<br>
Thrustmaster<br>
VKBsim<br>
VMware<br>
[安卓搞機工具箱](https://jamcz.com/gjgjx/)<br>
[Netmount](https://www.netmount.cn/download)<br>
[Volanta](https://volanta.app/)<br>
[Hash Checker](https://apps.microsoft.com/detail/9nblggh6csh2?hl=en-US&gl=US)<br>
[LG TV AutoControl](https://github.com/JPersson77/LGTVCompanion)<br>
[Fastcopy](https://fastcopy.jp)<br>
[Modengine](https://modengine.app)<br>
[Motrix](https://motrix.app)<br>
[Upscayl](https://upscayl.org)<br>

### Block Windows Update

Install "block_windows_update.reg"
open "Windows Update" > select pause date

### Privacy And Security Settings > OFF

### Notification > OFF

### Remove OneDrive Icon

Win+R > regedit > Ctrl+F > "018D5C66-4533-4307-9B53-224DE2ED1FE6 > u can see a DWORD(32) named "System.IsPinnedToNameSpaceTree" > change Hex from 1 to 0 > Restart File Explorer

### Storage Purify

Settings > Storage > open "Storage Sense"

### Keyboard Input

Settings > Time&Language > Typing > Advanced Keyboard Settings > Input Language Hotkey > Change Key Sequence > "Switch Input Language"->"Left Alt+Shift" and "Switch Keyboard Layout"->"Not Assigned"

### Windows Cursor Replace

### Close Heterogeneous Thread Scheduling

1.CMD execute "powercfg -attributes SUB_PROCESSOR 93b8b6dc-0698-4d1c-9ee4-0644e900c85d -ATTRIB_HIDE" and "powercfg -attributes SUB_PROCESSOR bae08b81-2d5e-4688-ad6a-13243356654b -ATTRIB_HIDE"<br>
2.Win+R > Control > Power Options > Change Plan Settings > Change Advanced Power Settings > Processor Power Management > change "Heterogeneous Thread Scheduling Policy" and "Heterogeneous Short running Thread Scheduling Policy" to "All Processor"

## Change-Anytime Config After Status

### Memory OC <Ref. value>

| Clock                | Voltage | TRC | TRFC |
| -------------------- | ------- | --- | ---- |
| 3200(13-18-18-18-36) | 1.45V   | 70  | 500  |
| 3400(13-18-18-18-36) | 1.45V   | 75  | 540  |
| 3600(14-19-19-19-38) | 1.45V   | 80  | 560  |
| 3800(15-20-20-20-40) | 1.45V   | 80  | 580  |
| 4000(16-21-21-21-42) | 1.45V   | 90  | 600  |

Trc 90
TrrdS 4
TrrdL 6
Tfaw 16
Twtrs 4
TwtrL 8
Twr 16
Trdrdscl 4
Twrwrscl 4
TRFC 600
Trtp 8

### r23 Ref.

| Single | 1465 |
| ------ | ---- |

| Multi | 14676 (15308) |
| ----- | ------------- |

### 9800X3D Optimization

主頁-EXPO-enable
高階模式-Ai Tweaker
Ai Overclock Tuner-EXPO Tweaker
FCLK Frequency-1/3 MEM frequency
AUSU performance enhancement-enable
Core performers boost-enable
F9 search: power down-All enable | memory context-All enable
高級-AMD overclocking
Precision boost overdrive-高級
PBO Limits-Motherboard
Precision boost overdrive scalar-6x
CPU bost clock override-enable(positive)
Max CPU boost clock override(+)-200
Platform thermal throttle limit-95
Curve optimizer-All cores-negative-20

### Customize Logitech G Hub install location

1.if we want install the hub in `D:\Program file`.We create a directory named `D:\Program file\LGHUB`under repository D.<br>
2.open powershell in administrator mode.<br>
3.goto root folder where logitech want to install:`cd 'C:\Program File`<br>
4.create symlink

```
New-Item -ItemType SymbolicLink -Path 'C:\Program Files\LGHUB\' - Value 'D: \Program Files\LGHUB\'
```

5.now run the .exe<br>
6.confirm the app installed there in rep C<br>

### macOS installed apps

AdGuard<br>
BaiduNetDisc<br>
BTT<br>
Clash Party<br>
Discord<br>
Equinox<br>
FCP<br>
Github Desktop<br>
HashCheck<br>
Ice<br>
IINA<br>
iMovie<br>
Keka<br>
KeyboardCleanTool<br>
KnockKnock<br>
LibreOffice<br>
LuLu<br>
Macs Fan Control<br>
Noir<br>
noTunes<br>
OKX<br>
OrbStack<br>
PDFgear<br>
PearClean<br>
Pixelmator Pro<br>
Privileges<br>
QQMusic<br>
Quark Disc<br>
Royal TSX<br>
Shottr<br>
Sloth<br>
Syntax Highlight<br>
Tempermonkey<br>
Telegram<br>
Tiny Image<br>
Tor Browser<br>
Typora<br>
Upscayl<br>
venera<br>
VSCode<br>
WArp<br>
