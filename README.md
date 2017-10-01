# appworld
![software store icon](https://cdn.rawgit.com/PapirusDevelopmentTeam/papirus-icon-theme/master/Papirus/64x64/apps/software-store.svg)

AppWorld is a central catalog of all Linux GUI apps. AppWorld does not discriminate between toolkits (GKT+/QT/Electron) and does not hold apps to a UI/UX standard. AppWorld apps are categorized and contain install scripts/instructions for most package managers and cross-platform distribution methods.

## Please Contribute
### Report Abandoned Apps
An app is considered to be abandoned if the last commit was more than a year ago *or* if the author has publicly declared it to be abandoned or discontinued. Please post an issue and/or pull request if there is such an app in the catalog.
### Contribute Apps
As you have probably noticed, this repository is currently empty. I will be adding some apps soon. However, anybody is more than welcome to submit a pull request, as long as they follow the guidelines below:
#### App Format
Each app has two files and two folders.
1. The `.appdata.xml` file describes the app in [AppStream format](https://www.freedesktop.org/wiki/Distributions/AppStream/) with some exceptions.
2. The `install.xml` describes how to install the application. See [#Installation](#installation) for more.
3. The `icons` folder has the app's logo in 64x64 and 128x128.
4. The `screenshots` folder has screenshots of the app for a variety of distributions. See [#Screenshots](#screenshots)

#### Installation
An app's `install.xml` file contains supported installation methods of the app described. Each installation method is one XML tag.
```xml
<ubuntu version="xenial" component="universe"> <!-- package name --> </ubuntu>
<fedora version="26"> <!-- package name --> </ubuntu>
<flathub> <!-- package name --> </flathub>
<snap> <!-- package name --> </snap>
etc
```

#### Screenshots
Each folder in the `screenshots` folder is named in `(gtk theme)-(icon theme)` format. The font should match the theme (eg `adwaita-adwaita` would use the Cantarell font). The default screenshot should be `adwaita-adwaita`. However, any other themes for different distributions are welcome.
