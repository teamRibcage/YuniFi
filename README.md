## End of Support

As Ubiquiti has now officially ended support for their "Legacy" user interface (which this theme was intended to complement), this repository is no longer being actively updated or maintained. Thank you to all who supported it!

# YuniFi
A [HomeAssistant](https://www.home-assistant.io/) theme inspired by Ubiquiti's UniFi interface and [aFFekopp](https://github.com/aFFekopp)/[noctis](https://github.com/aFFekopp/noctis)

![](https://raw.githubusercontent.com/teamRibcage/YuniFi/main/screenshots/desktop_1.jpg)

## Installation

#### Manual Installation
1. If you don't have one already, create a `themes` folder in your HomeAssistant directory
2. Copy the `YuniFi` folder from this repository into your `themes` folder
3. Add the following to your `configuration.yaml` file (if not already present)

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

3. Restart HomeAssistant
4. Select the YuniFi theme in your user's profile 

#### Font
If you would like to use the custom font (Lato) as defined in the theme:
1. Add the following to your `Lovelace Dashboards` configuration under the `Resources` tab 
```yaml
https://fonts.googleapis.com/css2?family=Lato
```
- Type = `Stylesheet`

## Screenshots

#### PC
![](https://raw.githubusercontent.com/teamRibcage/YuniFi/main/screenshots/desktop_2.jpg) | ![](https://raw.githubusercontent.com/teamRibcage/YuniFi/main/screenshots/desktop_3.jpg) | ![](https://raw.githubusercontent.com/teamRibcage/YuniFi/main/screenshots/desktop_4.jpg)
:----:|:----:|:----:

#### Mobile
![](https://raw.githubusercontent.com/teamRibcage/YuniFi/main/screenshots/mobile_1.jpg) | ![](https://raw.githubusercontent.com/teamRibcage/YuniFi/main/screenshots/mobile_2.jpg) | ![](https://raw.githubusercontent.com/teamRibcage/YuniFi/main/screenshots/mobile_3.jpg) | ![](https://raw.githubusercontent.com/teamRibcage/YuniFi/main/screenshots/mobile_4.jpg)
:----:|:----:|:----:|:----:

## Additional Information

#### Custom:Button-Card
The above screenshots rely heavily on [custom-cards](https://github.com/custom-cards)/[button-card](https://github.com/custom-cards/button-card) in their design. When using the Custom:Button-Card with this theme, button color behavior can be defined using variables such as `var(--base-colors-orange)` in your button configuration. These colors are defined in the `# Base Color Definitions` section of the `YuniFi.yaml` file. Example:

```yaml
state:
  - value: 'on'
    icon: mdi:pause-circle-outline
    color: var(--base-colors-orange)
```

See the Button-Card documentation for further information on card configuration

----

#### The Color Green
By default, this theme uses a "seagreen" shade of green for badges and graphs (I just like the color 😁). To match Ubiquiti's UniFi color scheme, simply change the variables in the two locations noted in the `YuniFi.yaml` file. Example:

```yaml
  # Feedback Colors
  success-color: 'var(--base-colors-seagreen)'  # <----- Change to 'var(--base-colors-green)' to match UniFi color
  warning-color: 'var(--base-colors-orange)'
  error-color: 'var(--base-colors-red)'
```
