---
title: "Router Setup"
permalink: /router_setup/
excerpt: "How to quickly install and setup the router for use in the Indigenous Language Robots project."


toc: true
toc_icon: "clipboard-list"
toc_label: "Steps"
toc_sticky: true
---

The router is responsible for setting up the local network used by all components of the robot to talk to each other.

## Unpacking the router

The router we are using in this project is a TP Link mini router TL-WR810N. When unpacking it, the box should contain:

- the router 
- one micro-usb cable (used for powering the router)
- one ethernet cable (we will use it later to connect the [raspberry pi](/ILR/rpi_setup/) to the router)

![router image](/ILR/assets/router/router.jpg){: .align-left width="50%"}  Prior to setting up the router, look at the back of it and note the SSID and password (they will be needed to connect to the router)

## Connecting to the router

Power the router and, from your computer, connect to it via Wifi (The network id and password will be the one at the back of the router)

Once your computer is connected to the router local network, open a web browser and type *168.192.0.1* to access the router settings page. The browser should display the page below:

![admin interface](/ILR/assets/router/router.jpg){: .align-center width="100%"}  

Enter the default login (*admin*) and password (*admin*) to access the router settings page.

**Note**: On TP Link wifi, the interface can also be accessed by typing *tplinkwifi.net/* in the browser. It is also possible to change the admin login and password from this interface (but not necessary for the robot to work).
{: .notice--info}

{% include figure image_path="/assets/router/1.png" alt="Screenshot of the router interface"%}

## Router settings


**Watch out** blabl blab labl
{: .notice--danger}


You can use the [editor on GitHub](https://github.com/CoEDL/ILR/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/CoEDL/ILR/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
