# Installation
This guide will help you install the the EliteVA plugin into your VoiceAttack environment.

## Prerequisites
Before we get started using EliteVA, a few things have to be set up.

### VoiceAttack
EliteVA is a plugin for VoiceAttack. If you do not have VoiceAttack installed yet, download it from the [VoiceAttack website](https://voiceattack.com/Default.aspx#download-1).

VoiceAttack does have a free version, but to make use of the full functionality of EliteVA, you will need to purchase a license for $10.00 (additional sales tax may apply).

Once VoiceAttack is properly installed, be sure to check the box labeled `Enable Plugin Support` found under the `General` tab of the VoiceAttack options menu.

### Zip file extractor
You will also need a tool to open and extract .zip archives. WinRAR is highly recommend. WinRAR is a powerful free tool that is very easy to use. You can download WinRAR for free from [win-rar.com](https://www.win-rar.com/start.html?&L=0) by clicking the blue download button.

The default Windows zip extractor is also sufficient.

## Downloading EliteVA
The latest version of EliteVA can be found on the [EliteVA Github releases page](https://github.com/EliteAPI/EliteVA/releases).

## Installing EliteVA
After the archive has finished downloading, open File Explorer and navigate to the .zip file you just downloaded.

Right click the `EliteVA.zip` file you downloaded and select `"Cut"`. Next, navigate to your VoiceAttack installation directory. This folder is located at the following paths by default:
```
C:\Program Files (x86)\VoiceAttack
```
```
C:\Program Files (x86)\Steam\steamapps\common\VoiceAttack
```

In the VoiceAttack folder should contain a directory called `Apps`, if not, create it.

In the `Apps` folder, and create a new directory named `EliteVA`. This will be the root folder for the plugin.

Open the `EliteVA` directory you just created, right click in the folder and select `"Paste"`. This will paste the `EliteVA.zip` file in the `EliteVA` folder.

Right click on the `EliteVA.zip` file and select `"Extract Here"` to extract the contents of the zip file into your `EliteVA` directory.

### Let's double check that
You should have the following files in your VoiceAttack directory:
```
VoiceAttack\Apps\EliteVA\EliteVA.dll
VoiceAttack\Apps\EliteVA\Bindings
```

Once you have installed those files, restart VoiceAttack.

If the install is performed correctly VoiceAttack should show some set of messages along the lines of:
```
Plugin support enabled
Initializing EliteAPI v3.X.X.X
EliteAPI has started
Plugin 'EliteVA' initialized
```

### Still having issues?
If these messages do not appear in VoiceAttack, double check that you followed the installation guide correctly. If problems still continue to persist contact, support can be found in the [EliteAPI discord](https://www.discord.gg/jwpFUPZ) for assistance.

## Best practices
Now that you have EliteVA properly installed, it is recommended to always start VoiceAttack prior to loading up Elite: Dangerous to ensure the API and any associated VoiceAttack profiles track the game's events as accurately as possible.

Fly dangerously, Commander.

**o7**
