# appworld
AppWorld is a central catalog of all Linux GUI apps. AppWorld does not discriminate between toolkits (GKT+/QT/Electron) and does not hold apps to a UI/UX standard. AppWorld apps are categorized and contain install scripts/instructions for most package managers and cross-platform distribution methods.

## Please Contribute
### Report Abandoned Apps
An app is considered to be abandoned if the last commit was more than a year ago *or* if the author has publicly declared it to be abandoned or discontinued. Please post an issue and/or pull request if there is such an app in the catalog.
### Contribute Apps
As you have probably noticed, this repository is currently empty. I will be adding some apps soon. However, anybody is more than welcome to submit a pull request, as long as they follow the guidelines below:
#### App Format
Each app has two files and an `icons` folder.
1. The `.appdata.xml` file describes the app in [AppStream format](https://www.freedesktop.org/wiki/Distributions/AppStream/).
2. The `install.xml` describes how to install the application. See [#Installation](#installation) for more.
2. The `icons` folder has the app's logo in all sizes.

#### Installation
An app's `install.xml` file contains all supported installation methods of the app described, ordered from most to least preferable. Each installation method is one XML tag.
```xml
<flatpakref> <!-- url to flatpakref --> </flatpakref>
<flathub> <!-- flatpak rdnn --> </flathub>
<snap> <!-- name of snap package --> </snap>
<appimage> <!-- url to appimage --> </appimage>
<official-repository>
    <distro-name> <!-- "distributor id" in 'lsb_release -a' --> </distro-name>
    <distro-version> <!-- "codename" in 'lsb_release -a' --> </distro-version> 
    <url> <!-- url of the repository --> </url>
    <component> <!-- the debian/ubuntu component (eg main, contrib, or multiverse) --> </component>
<official-repository>
<repository>
    <!-- same as official-repository -->
<repository>
<package-file>
    <type> <!-- either deb, rpm, or eopkg --> </type>
    <url> <!-- url of the file --> </url>
</package-file>
```
