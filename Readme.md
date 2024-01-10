# Music streaming analysis

## Project overview

This essence of this project is to gather some insights on the streaming data of music industry specially for the digital platform/application Spotify.
There are 2 major aspects covered in the project which are -
  1. Artists Performance
  2. Albums release strategy

## Data source

Artist & Album dataset - I have used this primary dataset which contains detailed information on the top tracks data, albums release data and Artist-Fans engagement data of 40 most popular Indian music artists.

## Tools

  -  Python - Data extraction through web API as well as data transformation into machine readable format
  -  Tableau - Generating meaningful insights from data and creating a human understandable report

## Data extraction & transformation

Through the use Spotify web API and python, the following code performed the web scraping method for data extraction:

      -  ```python
         #Process the data
         sp = Authenticate.spoauth(cid, secret)
         artist_source_data = music_data.artist_source_data('Artists data.csv')
         artist_top_tracks_data = music_data.Top_tracks_data(0,40,sp,artist_source_data)
         artist_genre_data = music_data.artist_genre_data(0,40,sp,artist_source_data)
         artist_album_data = music_data.artist_album_data(0,40,sp,artist_source_data).drop_duplicates()
         album_market_data = music_data.album_market_data(sp,artist_source_data).drop_duplicates()

         #Save the data
         music_data.artist_album_datasave("Artists data.xlsx")
         ```
         
## EDA (Exploratory Data Analysis)

EDA involves exploring the Artist & Album dataset to answer key questions such as -
  1. How much average popularity does the Indian artists share on the music streaming platform in respect to the global music streaming industry?
  2. Aggregating the last 10 years data, how much is the difference between the amount of album releases and an ideal Pareto 80/20 principle?
  3. Which are the regions across the world in which the albums were not released?
  4. When the topic is on artists interactions with the fans, which are the Indian artists that are known for strong positivity,enthusiasm and satisfaction among the fans?

## Data analysis

Here is an interactive tableau dashboard that I generated which shows the answers of above key questions in a visual format.

## References

1. [Introduction to computer science and programming](https://ocw.mit.edu/courses/6-00-introduction-to-computer-science-and-programming-fall-2008/download/)
2. Google Bard for understanding the EDA that can be performed in the music streaming industry
3. Basic to Advanced Tableau Dashboard Mastery Course by Jatan Shah
