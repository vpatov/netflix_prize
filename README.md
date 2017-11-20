The cleaner notebook cleans some of the input data, to make it easier to process.
The prediction notebook reads in the data and then makes the predictions.
Below is a summarized description of the file formats.


Combined_data has the ratings.
combined_data_i.txt format:

Movie_ID_1:
CustomerID,Rating,Date
CustomerID,Rating,Date
CustomerID,Rating,Date
...
Movie_ID_2:
CustomerID,Rating,Date
CustomerID,Rating,Date
CustomerID,Rating,Date
...

- MovieIDs range from 1 to 17770 sequentially.
- CustomerIDs range from 1 to 2649429, with gaps. There are 480189 users.
- Ratings are on a five star (integral) scale from 1 to 5.
- Dates have the format YYYY-MM-DD.

===============

Movie information in "movie_titles_cleaned.txt" is in the following format:

MovieID,YearOfRelease,"Title"

- MovieID do not correspond to actual Netflix movie ids or IMDB movie ids.
- YearOfRelease can range from 1890 to 2005 and may correspond to the release of
  corresponding DVD, not necessarily its theaterical release.
- Title is the Netflix movie title and may not correspond to 
  titles used on other sites.  Titles are in English.


===============
Test data set, in "qualifying.txt"
Supposed to predict for each of these.

MovieID1:
CustomerID11,Date11
CustomerID12,Date12
...
MovieID2:
CustomerID21,Date21
CustomerID22,Date22

What are the (predicted) ratings?

===============
Probe-Test dataset

MovieID1:
CustomerID11
CustomerID12
...
MovieID2:
CustomerID21
CustomerID22

Like the qualifying dataset, the movie and customer id pairs are contained in
the training set.  However, unlike the qualifying dataset, the ratings (and
dates) for each pair are contained in the training dataset.
