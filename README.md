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
## Changing the header color
Add this line to styles.css:

```
h1 {
  color: black;
}
```
What this does is that it changes the header color to black (or any color of your choice) for all the headers on your site that use this stylesheet. This creates a unified identity for the colors on your webpage! And you don't have to define it again and again for every new page you create. 

What this does is that it applies a styling to any h1 elements in the HTML document. Next we're going to link the styles.css sheet to the recipe page. Make sure you add it to all of your html pages.

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

![image](https://github.com/user-attachments/assets/89af1233-7f88-4e19-ba40-4df0eff8d993)

If your title looks black like this, you're on the right path!

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

![image](https://github.com/user-attachments/assets/429a9155-1a86-41a3-a9e5-3587a8610d3a)

Much better! Now the text is at the bottom of each picture instead of to the side. But I think we can do so much better, so let's add another flexbox to align these recipes side by side.

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
    <div class="container">
      <div class="recipe">
            <img src=https://rakskitchen.net/wp-content/uploads/2014/06/14336259454_504e87ce37_z.jpg>
            Baingan Bharta
      </div>
      <div class="recipe">
            <img src=https://www.cookerru.com/wp-content/uploads/2022/06/mapo-tofu-recipe-preview-feature-500x500.jpg>
            Mapo Tofu
      </div>
    </div>
</body>
```

In styles.css, add this:
```
.container {
    display: flex;
    justify-content: center; /* centers horizontally */
    gap: 20px;
}
```

![image](https://github.com/user-attachments/assets/4ed80cd3-00dc-4dbf-8adc-d338e8d99019)

Feel free to add more recipes that you like! I just started with two just to show as an example.

## Show your favorite recipe!

Now that you have a list of recipes, pick a favorite and highlight in gold!
Add these lines of code to your styles.css:

```
.favorite-recipe {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 5px;
  background-color: gold;
}
```

And for your favorite recipe, change the div class from "recipe" to "favorite-recipe". For mine, I chose baigan bharta!
![image](https://github.com/user-attachments/assets/47adcb7c-06d4-4f4b-b08f-8e3645278436)

If you need to see the whole code at some point, here's the trinket link: https://trinket.io/html/ea98da3de175 

## Extra Challenge

Try making it so that whenever a user clicks on a recipe, it links them to a different page! It can be either a page that you create or an external website.













