# Data-Visualizations-with-Spotify-Data-in-Python
Creating Data Visualizations with Spotify Data with Python


I am using the "Streaming History0" and "YourLibrary" files from my Spotify account.

Goal:

Import Excel data.

What day of the week are songs streamed most?

Top 10 Streamed Songs.

Top 20 Streamed Artists.

How many songs belongs to each artist on your library ?

Steps for preparing Data "StreamingHistory0":
1. Convert files from json to xlsx.
2. Delete "record" column in Excel.
3. Add a "date" column:  
     =LEFT(A2,FIND(" ",A2,1)-1)
4. Add a "wkday" column: 
     =CHOOSE(WEEKDAY(B2),"Sun","Mon","Tue","Wed","Thu","Fri","Sat")
5. Add a "time" column: 
     =RIGHT(A2,FIND(" ", A2,1)-6)
6. Add a "minsPlayed" column: 
     =G2/60000
7. Add "Include Song" (songs played less than 2 min): 
     =IF(H2 >2,"Yes","No")
