***This repository contains the data and notebooks for my personal experiment to scrape the website for Fabled Game Studios' card roguelike, 'Pirates: Outlaws'.***

The code in the `notebooks` folder performs the following functions:

`pirates_outlaws_bot` -  *Scrape the website of the game 'Pirates: Outlaws', get to the Relics page, and store all the webpage results. Then process them with xpath to scrape the name of each relic and its effect, storing it within a csv file for each map in the game. Don't mind the last section, it's in case the website throws a timeout for the last couple of entries*

`all_relics_csv_create` - *Compiles a merged .csv file for all the relics, adding in features derived from the `Effects` column, from things like relics that cause card draw or health regeneration or defense increase, to relics that have limitations during gameplay. These features are added in as columns with the Boolean values of `True` or `False` for each relic, denoting whether the specific effect is present.*

`divide_by_effect` - *Derives separate .csv files for each relic separated by their corresponding effect. For instance, the .csv file named `relics_with_randomness` will contain all the relics that have the value `True` when the value of the column `Randomness` is checked.*



**In addition, this repository contains the results of each step:**

`webpages-pickled` - *Contains the pickled webpages as stored in `pirates-outlaws-bot`.*

`relics-by-map` - *Contains the .csv files of relics sorted by their maps as stored in `pirates-outlaws-bot`, as well as the merged list of relics, `all_relics.csv` that is derived from `all_relics_csv_create`*

`relics-by-effect` - *Contains the .csv files of relics sorted by their effect as stored in `divide-by-effect`*
