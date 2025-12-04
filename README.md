# Stardew-Valley-Recipe
Knowing exactly what to do with collected items in a video game can be difficult. With Thanksgiving occurring and Tableau’s Iron Viz food theme happening, I knew I had to try and craft a traditional recipe style book.  



https://github.com/user-attachments/assets/f0567cff-8ddb-483b-bb5e-4da2da7f8d32


### Finished Product ###
You can view and use the dashboard yourself [here](https://public.tableau.com/app/profile/marissa.nash/viz/Recipe_17608034631380/Dashboard1)


### Inspiration ### 

I was inspired by Brittany Rosenau’s [Tillable Tiles](https://public.tableau.com/app/profile/brrosenau/viz/StardewTillableTiles/StardewTillableTiles). When I saw she collected the data from the Stardew Valley wiki, I jumped on the opportunity to see what interesting data the wiki had to offer. As a foodie myself, I was drawn to the cooking category. <br> 

As someone who has played Stardew Valley, I liked the idea of looking in your inventory and asking, **what can I cook with what I have?** This drove the inspiration for the “Search” portion of the project.  <br> 

 <img width="399" height="298" alt="image" src="https://github.com/user-attachments/assets/a6031850-b690-42fe-b939-368ff944da0d" />

Then, I thought it would be neat if you could look at the recipes searched as if they were in a cookbook! The above image is similar to what I was imagining in this sense. <br> 

### Programs Used ### 

- Excel for data collection and cleaning 

- Tableau for visualization 

### Scope of Work ### 

**Deliverables** <br> 

- Cleaned Dataset of recipes and associated ingredients’ 

- Dashboard with the ability to search ingredients, click on organized tabs, and see recipe details 

### Goals ### 

I liked that the data was relatively simple for this dataset. I wanted to convey the information in a more exciting way outside of a table and see what I could create using this data. The idea of a search box was particularly appleaing and I just kept wanting to expand my skills in the area. Learning that Iron Viz was a food theme and due in a week was a great kick in the butt to put more time into this project and complete it.  

### Data Source and Collection ### 

Turns out, there are a few wikis for Stardew valley! <br> 

I got the data initially from [here](https://stardewvalley.fandom.com/wiki/Stardew_Valley_Wiki), then in my cross verification on the offical website [here](https://stardewvalleywiki.com/Stardew_Valley_Wiki), I came upon a few conflicting variables. So, I had to go through and verify each entry and add a few that the initial dataset left out. This was great to ensure data quality, but it took extra time. I imported the table on the wiki into Excel, cleaned up the categories I didn’t need, and separated the ingredients into separate observations. Over the course of the visualization, I also had to reformat the source data in a few different ways to accommodate what I was trying to visualize.  

### Viz Design and Creation ### 

This viz really explores parameters and parameter actions. A big goal for me was querying a whole database using a search bar. To do this, I created a string parameter that took all values. To give the user some ideas, I kept the current value as “Egg, milk, wheat flour”, three common ingredients used in Stardew Valley recipes. I used a calculated field to communicate with this parameter to collect recipes with the keywords the user typed in. Below is an example formula used in the calculated field created for the search bar. 

IF { FIXED [Recipe] : MAX(CONTAINS(LOWER([Ingredient Search]), LOWER([Ingredients]))) } THEN TRUE 

ELSE FALSE END 

This felt like a relatively simple way to accomplish a “search bar”! 

I wanted to display details of the recipe when it was selected. Similar to the inspiration photo! That way a user could click on a recipe they’re interested in to see relevant details that Stardew Valley fans would want to know! For instance, where to get the recipe, how much health/energy the recipe would restore, and what the recipe would look like when crafted. Additionally, I chose to add the cute little examine sentence included when you cook the item like the way traditional cookbooks would!  

Recipe details were crafted using a lot of text marks, formatting, and a show/hide parameter on a floating container. Additionally, I realized that sometimes a user doesn’t even know where to begin. So, I once again considered what the end user would appreciate. With this I created on the theme “tabs” that a well-used cookbook would have. These included ways to show top 10 recipes that provide health, energy, short one-ingredient options, and a dessert tab because who doesn’t love dessert? 

Because the ingredient search bar was tied to the main recipe tab, I basically had to rebuild the recipe tab again but for the tabs. This made it difficult to display the “tabbed” recipes and the searched recipes at the same time. I utilized [this guide](https://thedataschool.com/a/harry-osborne/sheet-swapping-in-tableau/) to help successfully collapse and effectively “hide” the recipe display. This definitely took some fiddling with containers and sizing, but we accomplished it pretty seamlessly! 

 

### Reflection ### 

A lot of calculated fields and parameter actions really “clicked” with this project! I enjoyed finally having a good understanding of these concepts and I think it will really help me in the future. I think this more educational visualization was a great way to work with simple data but more complex UI elements that have a surprisingly important place in the data analysis world. I’m also proud to have submitted it to the Iron Viz 2026 competition as it will boost my visibility and beyond my newfound degree, formally says “hey, she’s a data analyst!”. For a business and stakeholder angle, imagine the data was querying certain item SKUs instead of recipe ingredients! You could view a specific item’s sales performance or flow effectiveness through a supply chain network! There are many use cases for something like this! 😊  

 
