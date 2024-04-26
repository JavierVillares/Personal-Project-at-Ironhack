# Personal-Project-at-Ironhack
Personal Project of Javivi at Ironhack. Original timeframe Mon 22 April - Friday 26 of April 2024
-In this project if have expanded on the idea of "https://datasets.wri.org/dataset/globalpowerplantdatabase" where they have created a data base of most of the powerplants sorted throughout the world that are on grid level of energy production (energy output higher than 1MWh) where we are going to add 2 columns. (even though we could just add one) of the cost of co2 per gwh produced for each powerplant with in a certain year.

Sadly there are so many isnull values for so many years. We have decided to start off with the power estimations of 2017 where they used machine learning and fancy algorithms of science to calculate how much energy output each power plant would have produced with in that year. 

After doing some comparison (we took the power estimation of the power plants that have actually a valid input for that year. In this case 2017) we saw that there isn't much of a discrepency between real values and the estimation. In most cases there is a overestimation (but taking into account that the difference is more or less 10%-15% higher than actual measeured values). This is taken into account but crosschecking how much the electricity production world wide has grown over these years (2024 as of writing this read me) it´s more in line for current years. If most of the powerplants within the list are still operational. Some further investigation would be necessary. https://yearbook.enerdata.net/electricity/world-electricity-production-statistics.html ("Proof of concept of energy increase from 2017 to 2022")


-All of the csv's ar neatly stored in a file seperatly to give a bit of small overview of what we can find in this project.

After webscraping "https://www.cowi.com/about/news-and-press/comparing-co2-emissions-from-different-energy-sources" and "https://en.wikipedia.org/wiki/Life-cycle_greenhouse_gas_emissions_of_energy_sources" about the life cylce of co2 amongst the different primary fuel types of the powerplants we found a mean (for Oil we had to use the median of wikipedia). Both sources have quoted "https://www.ipcc.ch/" as sources. 

-Cleaning notebooks are stored with in the "cleaning notebooks" file. 

After having cleaned every data and making the proof of concept work we worked on merging everything together into one Dataframe. The only columns within that dataframe are "country_long", "name" => (name of the powertplant), "primary_fuel", "estimated_generation_gwh_2017", "CO2e/KWh" => (we had to convert everything from g/kwh to Mt/GWH but at the end it's just multiplying the correct measurements and tripplechecking everything), "Total MtCO2" => And finally the culmination of everything. The calculation of everysingle powerplant taking into account the fuel_type and how much it has produced in GWh. 

With this we can expand onf everything. 

Further plans are to find how much it would cost each citizen (depending on the country) to pay for a carbon tax taking into account what the electricity in that grid is pulling from. In the most utopian and ideal scenario this carbon tax would be charged only and only from the companies that are providing this energy to the citizens but we all know this will not work. The carbon Tax should go to a government fund that invests in greener energy types. Red taping carbon intensive energy productions, and green lighting all the projects necessary to modernize the grid, making it more modular and smarter. 

There are many options we can play with. We encourage anyone if this project is of use for in any way please use it.

Credits : 

Global Power Plant Database => "https://datasets.wri.org/dataset/globalpowerplantdatabase"
Cowi.com => "https://www.cowi.com/about/news-and-press/comparing-co2-emissions-from-different-energy-sources"
Wikipedia => "https://en.wikipedia.org/wiki/Life-cycle_greenhouse_gas_emissions_of_energy_sources"
The Intergovernmental Panel on Climate Change => "https://www.ipcc.ch/"
Data Analyst = Javier V.Z.