# New York County Took the Majority Hit for Job Losses in the State

### Write your nutgraf here

Make sure your pitch answers the following questions:

- Why this story is relevant ("So what?) and why now?
- What is the single question your story tries to answer?
- Why will this story resonate with your audience?

What else has been done on this topic (provide links)? How is your angle different or fresh?

- [Industries hit hardest by coronavirus in the US include retail, transportation, and travel (USA TODAY)](https://www.usatoday.com/story/money/2020/03/20/us-industries-being-devastated-by-the-coronavirus-travel-hotels-food/111431804/)
- [Three Industries That Are Being Decimated By The Coronavirus (Forbes)](https://www.forbes.com/sites/chuckjones/2020/03/28/three-industries-that-are-being-decimated-by-the-coronavirus/#3f186cd79423)
- [These Industries Suffered the Biggest Job Losses (CNBC)](https://www.cnbc.com/2020/05/08/these-industries-suffered-the-biggest-job-losses-in-april-2020.html)

Describe how and where you found the data with links to sources. Put the raw data (csv format) in a folder called `data` in this folder. Make a folder called `notebooks` where you will write your pandas code.

Write up at least one or up to three findings from your analysis based on the data you found.

- Finding 1: Of New York States businesses affected, 72% of hotels and 71% of restaurants affected were in New York County.
- Finding 2: For New York County number of affected for Restaurants was 28102 and hotels was 12690.                            - Finding 3: From the rows that had correct input data: For the hotel industry, the total percentage of employees laidoff for New York State was 66.4%, for the restaurant industry, the total percentage of employees laidoff for New York State was 13%. 


# Who are some potential human sources you could reach out to for more info?
Industry experts. economists that work or a staffer that works at a data analytics platform for one of the industries for example DAT Freight Analytics for transport jobs. 

# What is the maximum (best) story possible? What's the minimum (fallback) story if your hypothesis doesn't prove out?

Best story possible is to be able to narrow down percentage wise the actual affected number to see which indury really got hit based on how many are employed in that industry and how many were let go. Fallback is to just look at general numbers porvided in the data without suing percentages to get a better look. 

## How to publish and submit your project

1. Make sure you have navigated to your `data-journalism` folder with your terminal first. Clone a fresh copy of this template and navigate to the folder.

   ```
   git clone git@github.com:JOUR73351/ny-warn-scraper.git
   cd ny-warn-scraper
   ```

2) Remove my git tracking from the project

   ```
   rm -rf .git
   ```

3) Create a new repository on GitHub called `ny-warn-scraper` with the following settings.
   <br>
   <img src="assets/newrepo.png" width="500">

4) Run these git commands to initialize the repo. Make sure you've checked `ssh`.

   ```
   git init
   git add -A
   git commit -m "first commit"
   git remote add origin git@github.com:YOUR-USERNAME-HERE/ny-warn-scraper.git
   git push -u origin master
   ```

5) Write your pitch in `README.md`.

6) Run `pipenv install` to install all of the python dependencies and run `pipenv run jupyter lab` to start Jupyter.

7) Scrape the [WARN notices](https://labor.ny.gov/app/warn) from the NY Department of Labor website and output to `data/warn.csv`. Your scraper code will live in `notebooks/scrape.ipynb`.

   Extra credit if you can scrape previous years' notices as well. Here's a clue:

   ```
   https://labor.ny.gov/app/warn/default.asp?warnYr=2019
   https://labor.ny.gov/app/warn/default.asp?warnYr=2018
   https://labor.ny.gov/app/warn/default.asp?warnYr=2017
   ...
   ```

   Can you do this in a loop?

8. Come up with some questions about the data and try to answer them with pandas functions. Analyze the data you've scraped in `notebooks/analyze.ipynb`. You will probably need to do a bit of data cleaning in pandas and convert some columns to integers. Export the data you are visualizing in a chart in the `output` folder.

9) Write your story in and add your assets and charts to `index.html`. Feel free to play around with and change the styles in `style.css`, but you are not required to. Delete the code that you don't need for your story. The story itself should be no less than 150 words and include at least one chart from Datawrapper. You can embed a Datawrapper chart in your story by copying the embed code into your html as I have done in `index.html.`
   <br>
   <img src="assets/datawrapper.png" width="500">

10) You can preview a local version of your story by running a python server.

```
python -m SimpleHTTPServer 8000
```

Then, navigate to `http://localhost:8000` in your browser. Before step 8, you must quit the python server by pressing `ctrl+c`.

11. To save a version of your story on GitHub, run the following git commands.

```
git add -A
git commit -m "YOUR-COMMIT-MESSAGE-HERE"
git push
```

12. To publish, go to the settings of your GitHub repo, scroll down to GitHub Pages, and configure the source to the master branch.
    ![GitHub Pages](assets/ghpages.png)
