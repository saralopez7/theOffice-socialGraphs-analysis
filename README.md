# The Office Analysis

## See notebook in Nbviewer
You can also open the notebook in Nbviewer: [Nbviewer notebook](https://nbviewer.org/github/saralopez7/theOffice-socialGraphs-analysis/blob/master/The%20Office%20Analysis.ipynb)

##  Analysis of the American TV series "The Office"

For this project, we chose to analyse the American TV series **The Office**, the most-watched series across streaming in 2020, with 57.1 billion minutes streamed. This includes detailed season and rating statistics, character statistics, relationships and their influence on the success of the show measured in terms of IMDb ratings and views. We present our analysis through interactive visualizations we created using Plotly. 

We used four datasets:

## Dunderpedia: The Office Wiki
Encyclopedia dedicated to housing an informative database for all subject matter related to The Office

- Using [**Dunderpedia: The Office Wiki**](https://theoffice.fandom.com/) we first extracted all the characters that played in The Office from season 1 to season 9 (final). Besides, we downloaded the description of each character.     

## IMDb 
IMDb Ratings of The Office

- Using [**IMDb**](https://www.imdb.com/title/tt0386676) we made AJAX requests and using BeautifulSoup we extracted information about every episode of every season of The Office. This includes episode titles for all seasons, IMDb ratings, total votes, description and air date of every episode. 


## Kaggle: The Office Dataset
Dataset of all episodes of the popular US TV Series - The Office

 - From [**Kaggle**](https://www.kaggle.com/nehaprabhavalkar/the-office-dataset), we downloaded The Office dataset to extend the previously downloaded IMDb data. The new data includes guest stars, directors and writers. 
 
  It is important to note that even though this Office dataset from Kaggle also contains the ratings and Viewership of the Office, it has not been updated since `September 2020`. Therefore, we wanted to extract these data directly from IMDb to have the most up-to-date ratings and views. Since The Office is still available on Network and has been watched 50.1 billion times in 2020, these ratings are likely to be changing frequently. Hence, from this Kaggle dataset, we only took the static data: guest stars, writers and directors. 

##  Kaggle: The Office (US) - Complete Dialogue/Transcript
45,000+ lines of dialogue from 9 seasons of The Office

 - To further analyse the episode ratings, we needed information about the episode itself, such as the cast for each episode and the lines for each character in every episode. This is collected from the [**Kaggle dataset: The Office (US) - Complete Dialogue/Transcript**](https://www.kaggle.com/nasirkhalid24/the-office-us-complete-dialoguetranscript/version/1?select=The-Office-Lines.csv).

## Website

We have put together a website explaning the contents of the notebook: https://gallant-ride-ed7fdb.netlify.app/

The analysis posts can be found here: https://gallant-ride-ed7fdb.netlify.app/blog/



## What does this repository contain? 


The main notebook with the analysis is [The Office Analysis.ipynb](The%20Office%20Analysis.ipynb). 

Other sub-notebooks were created to keep the main notebook clean and short (to the greatest possible extend): 

- For data collection and preprocessing of the Dunderpedia Wiki source: [Preprocessing_Dunderpedia.ipynb](Preprocessing_Dunderpedia.ipynb). 

- For data collection and preprocessing of IMDb data for The Office and Kaggle: The OfficeDataset : [Preprocessing_IMDB_Kaggle_Office.ipynb](Preprocessing_IMDB_Kaggle_Office.ipynb). 

- For data collection and preprocessing of Kaggle:  *The Office (US) - Complete Dialogue/Transcript*: [Preprocessing_KaggleTranscripts.ipnynb](Preprocessing_KaggleTranscripts.ipynb)

- For tokenization of the character pages of Dunderpedia:  [DivideDocumentIntoTokens.ipnynb](DivideDocumentIntoTokens.ipynb)



# Installation 
1. This installation assumes that the Python3 is already installed. Otherwise please install them before continuing to next steps.
2. Clone the git repository
	```
	git clone https://github.com/saralopez7/theOffice-socialGraphs-analysis -b master
    cd theOffice-socialGraphs-analysis
	```
3. Install the dependencies
	```
	python3 -m pip install -r requirements.txt
	```

    Or if you are using conda: 
    ```
    conda install --file requirements.txt
    ```
4. Start Jupyter notebook.
4. Open [The Office Analysis.ipynb](The%20Office%20Analysis.ipynb). 

