# Triple Peaks Coffee Shop

This is the second project of the Software Engineering program at TripleTen. It was created using HTML and CSS, based on the design brief.

## Project features

- Semantic HTML5
- Flexbox
- Positioning
- Flat BEM file structure
- A custom form
- CSS animation and transform

## Recent Updates

We have created a navigation menu, a header and image, a recipes menu with multiple embedded videos, and a _Book a Table_ section with makes use a of reservation form.

Here's the header:
![image](/images/demo/header-image.jpeg)

Here's the recipes with embedded videos:
![image](/images/demo/recipes-image.jpeg)

One of the more intersting aspects of the project has been our extensive use of Githhub and also interacting the terminal.

Probably an entire course could be taught on Github. It's a criticall safeguard against software engineers against accidentally corrupting a project. It allows us to save each version of the project in a remote repository on Github and revert back to a previous version of the project if necessary. It's lika a cloud for software engineers.

Here's a sample interaction with Github in the terminal as I am writing this README file:

![images](/images/demo/terminal.jpeg)
In this example above I am seeing what images are in our project and then I am getting the status of our project. It then show that some changes have been made locally to the README.md file.

We also made extensive use of emmet extensions and multi-cursor selectors in Visual Studio. Emmet extension are shorthand ways to declare elements in code and save tons of time.

For example if I typed this:

`label.checkbox__label`

It would automically become:

`<label for="" class="checkbox__label"></label>`

multi-cursor selectors allow you to change multiple lines of code simulatenously. You can do so on a Macbook by selecting a line and then highlting other lines manually using the control button, or by hitting the CMD + Shift + L keys.

You can also have it highlight the next occurence of a word using CMD + D. This last two are especially useful for renaming classes all at once rather than having to do so individually which becomes prone to error.

Here's an **example of multi-cursor selectors** in use changing class name for a label element:

![images](/images/demo/multicursor.gif)

We were able to add a **menu**:
![menu](/images/demo/menu.jpeg)

We were also able to add an **animation** to the project as seen here:
![images](/images/demo/pulsate.gif)

This was achieved using a **BEM modifier** to a circle elemnet. CSS doesn't support circles natively to sou have to make a square with a **border-radius of 50%** as seen here.

```
.about__circle {
  width: 426px;
  height: 426px;
  background-color: #1878dc;
  border-radius: 50%;
  position: absolute;
  left: -129px;
  top: -152px;
  margin: 0;
}
```

He made use of a keyframe animation we named **pulsate**:

BEM Modifier is seen below

`<div class="about__circle about__circle_animation_blurred"></div>`

Here's the keyframes declaration in CSS an the animation attributs:

```
@keyframes pulsate {
      0% {
      transform: scale(1);
      opacity: 0;
      }
      50% {
      opacity: 0.6;
      }
      100% {
      opacity: 1;
      transform: scale(1.4);
      }
    }

.about__circle_animation_blurred {
  animation: pulsate 1.3s ease-in-out 0s infinite alternate;
}

```

Here's a breakdown of what the animation attirbutes do:

- **pulsate** calls the keyform we created called pulsate
- **1.3s** is the duration
- **ease-in-out** means the animation starts and finished at a slower pace than during the middle
- **infinite** is the number of times the animation runs
- **alternate** is the behavior of animation at the end of each cycle-- in thise case it does the opposite after each cycle

Lastly we included a footer which had links to our contact information.

## Instructions on Deployment

In order to use the code, we must have terminal access, a Github account, and a code editor. To make best use of the emmet extensions shown above you need to have an emmet extension installed in your code editor.

I am using Visual Studio on my macbook and so I have the "Emmet Live" extension by Yurii Semeniuk installed. It works well.

If you are new-- access to an AI tool (we are using Dot on a Discord server) can help you debug your your code or help you find github and terminal commands.

## Plan on improving the project

This project could potentially be improved through the ability to process payments online.
