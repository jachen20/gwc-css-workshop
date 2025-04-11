# Workshop #2 - Creating Stylesheets with CSS
Last tutorial we used a stylesheet from a website. This week we will focus on making our own! If you are new or haven't completed the tutorial from last week, please refer to it here: https://github.com/drshika/gwc-html-workshop. You can also copy it and use it for this lesson!
## Creating new files
1. Go to Trinket and sign in as usual! Click on the plus sign to add a new file called styles.css

![CSS](https://github.com/user-attachments/assets/f46cbc20-e28e-4032-9780-97270c8861c0)

Create another file called recipes.html and copy this code in.
```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projects</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.2/new.min.css">
    <link rel="stylesheet" href="https://fonts.xz.style/serve/inter.css">
</head>
<body>
<header>
    <h1>Recipes</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="projects.html">Projects</a>
            <a href="recipes.html">Recipes</a>
        </nav>
    </header>
</body>
```
![image](https://github.com/user-attachments/assets/3b4c6d53-a6e3-425d-b8b6-71d32c60c42d)

Make sure to also add this line in the navigation bar to all of the other HTML pages so that you can navigate to your new page from anywhere.
```
            <a href="recipes.html">Recipes</a>
```
## Changing the title color
Add this line to styles.css:

```
h1 {
  color: red;
}
```

What this does is that it applies a styling to any h1 elements in the HTML document. Next we're going to link the styles.css sheet to the recipe page.

```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projects</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.2/new.min.css">
    <link rel="stylesheet" href="https://fonts.xz.style/serve/inter.css">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
<header>
    <h1>Recipes</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="projects.html">Projects</a>
            <a href="recipes.html">Recipes</a>
        </nav>
    </header>
</body>
```

![image](https://github.com/user-attachments/assets/b3fa2fde-2343-4683-991c-d83c3dac410c)

If your title looks red like this, you're on the right path!

## Adding flexboxes

Flexboxes are useful for providing a layout/grid that can adjust to different display devices and screen sizes. For a more in-depth explanation as well as a list of all the things you can do with them, feel free to look here: https://css-tricks.com/snippets/css/a-guide-to-flexbox/

In the body of recipes.html, we'll make two new **divs**, which you can think of it as a container for HTML elements. You can search for any images of food on Google that you like! I just chose Baigan Bharta and Mapo Tofu as examples.

```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projects</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@exampledev/new.css@1.1.2/new.min.css">
    <link rel="stylesheet" href="https://fonts.xz.style/serve/inter.css">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
<header>
    <h1>Recipes</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="projects.html">Projects</a>
            <a href="recipes.html">Recipes</a>
        </nav>
    </header>
      <div class="recipe">
            <img src=https://rakskitchen.net/wp-content/uploads/2014/06/14336259454_504e87ce37_z.jpg>
            Baingan Bharta
      </div>
      <div class="recipe">
            <img src=https://www.cookerru.com/wp-content/uploads/2022/06/mapo-tofu-recipe-preview-feature-500x500.jpg>
            Mapo Tofu
      </div>
</body>
```

![image](https://github.com/user-attachments/assets/4fcc7fbd-18c2-4f81-83d6-65ca03e1e105)

On first glance, it does look weird, doesn't it? Once we add this styling below to styles.css, it should look a lot better:

```
.recipe {
  display: flex;
  flex-direction: column;
  align-items: center;
}
```







