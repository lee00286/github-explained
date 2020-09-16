# Font Awesome

## Table of Contents

1. [What is Font Awesome](#what-is-font-awesome)
1. [How to Use Font Awesome](#how-to-use-font-awesome)
1. [Font Awesome CDN](#font-awesome-cdn)
1. [Font Awesome Prefix](#font-awesome-prefix)

---

## What is Font Awesome

* [Font Awesome Version 4](https://fontawesome.com/v4.7.0/)
* [Font Awesome Version 5](https://fontawesome.com/)

---

## How to Use Font Awesome

### Web Fonts with CSS

You can use font awesome through [Web Fonts with CSS](https://fontawesome.com/how-to-use/on-the-web/setup/hosting-font-awesome-yourself#using-web-fonts). `/css/all.css` file contains the core styling plus that you will need.

Copy the path to `/css/all.css` file.

Put the line below in `<head>` of your HTML. Don't forget to replace `PATH-TO-FONT-AWESOME` with the path you copied.

```
<link rel="stylesheet" href="PATH-TO-FONT-AWESOME/css/all.css">
```

You can customize the line by refering to some [examples](https://fontawesome.com/v4.7.0/examples/).

---

## Font Awesome CDN

[Login](https://fontawesome.com/account/) and use the [CDN Picker](https://fontawesome.com/account/cdn) to get CDN URL like the line below:

```
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.14.0/css/all.css" integrity="sha384-HzLeBuhoNPvSl5KYnjx0BT+WB0QEEqLprO+NBkkk5gbc67FTaL7XIGa2w1L0Xbgc" crossorigin="anonymous">
```

---

## Font Awesome Prefix

When you use font awwesome icons, it is important to specify the icon's name and use the proper prefix.

### Version 4

In Version 4, `fa` was the only prefix used. Use the line below by replacing `ICON` with icon's name.

```
<i class="fa fa-ICON"></i>
```

### Version 5

In Version 5, there are three styles of icon and brand icon separated.

Below is a summary of prefix and its usage:

| New Prefix | Icon Style | SVG + JS Filename | Web Font Filename | Availability |
| --- | --- | --- | --- | --- |
| `fab` | Font Awesome Brands | `brands.js` | `fa-brands-400.*` | Free |
| `fas` | Font Awesome Solid | `solid.js` | `fa-solid-900.*` | Free |
| `far` | Font Awesome Regular | `regular.js` | `fa-regular-400.*` | Pro only |
| `fal` | Font Awesome Light | `light.js` | `fa-light-300.*` | Pro only |
| `fad` | Font Awesome Duotone | `duotone.js` | `fa-duotone-900.*` | Pro only |

You can use these prefix inside HTML code by using the lines below.

```
<i class="fab fa-ICON"></i>
<i class="fas fa-ICON"></i>
<i class="far fa-ICON"></i>
<i class="fal fa-ICON"></i>
<i class="fad fa-ICON"></i>
```

:memo: Some icons have been renamed in Version 5. If you want to use the new icon name, make sure to use the new `fab` prefix. You can check [Icon Name Changes Between Version 4 and 5](https://fontawesome.com/how-to-use/on-the-web/setup/upgrading-from-version-4#name-changes) to replace icon names.
