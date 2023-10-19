# Brea Pilcher SQLProjects

<h2></h2>
 
<h2>Description</h2>
All projects encompasses a SQL-based interactive experience guiding users through querying. 
<br />


<h2>1.Box office hits database</h2>

- <b>Q: This database contains an incomplete list of box office hits and their release year. In this challenge, you're going to get the results back out of the database in different ways! In this first step, just select all the movies.
 </b>
 
- <b>A:SELECT* FROM movies; </b>

- <b>Q:Now, add a second query after the first, that retrieves only the movies that were released in the year 2000 or later, not before. Sort the results so that the earlier movies are listed first. You should have 2 SELECT statements after this step.</b>

- <b>A:SELECT* FROM movies WHERE release_year > 1999 ORDER BY release_year ; </b>

<br/>
<img src="https://i.imgur.com/4adSZsM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<h2>2.TODO list database stats </h2>

- <b>Q: Here's a table containing a TODO list with the number of minutes it will take to complete each item. Insert another item to your todo list with the estimated minutes it will take.</b>

- <b>Q:Select the SUM of minutes it will take to do all of the items on your TODO list. You should only have one SELECT statement. </b>

- <b>A:SELECT SUM(minutes) FROM todo_list ; </b>

<br/>
<img src="https://i.imgur.com/aa4ZNyR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<h2>3. PROJECT: Design a store database </h2>

- <b>Q:Create your own store! Your store should sell one type of things, like clothing or bikes, whatever you want your store to specialize in. You should have a table for all the items in your store, and at least 6 columns for the kind of data you think you'd need to store. You should sell at least 6 items, and use select statements to order your items by price and show at least one statistic about the items. </b>

- <b>For my store , I chose to do an chothing store. I followed the directions above</b>

<b> Here is my code </b>

<br/>
<img src="https://i.imgur.com/hEFVU0i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/JjeNM4h.png"height="80%" width="80%" alt="Disk Sanitization Steps"/>
- <b>Here's the 6 columns </b>


<br/>
<img src="https://i.imgur.com/YFC5UN0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

- <b>Here's my 6 items ( I chose to do 15 clothing items for my store ) </b>

<br/>
<img src="https://i.imgur.com/YEXnfrT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/PkzwxqD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<h2>4. Karaoke song selector</h2>

- <b>step 1 - Ever sung karaoke? It's a place where you sing songs with your friends, and it's a lot of fun. We've created a table with songs, and in this challenge, you'll use queries to decide what songs to sing. For the first step, select all the song titles.</b>

- <b>A:Select title from songs ;</b>

<br/>
<img src="https://i.imgur.com/MfVAuTV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

- <b>Step 2 - Maybe your friends only like singing either recent songs or truly epic songs. Add another SELECT that uses OR to show the titles of the songs that have an 'epic' mood or a release date after 1990.
</b>

- <b>A: SELECT title FROM songs Where mood = 'epic' or released > 1990 ; </b>

- <b>Step 3- People get picky at the end of the night. Add another SELECT that uses AND to show the titles of songs that are 'epic', and released after 1990, and less than 4 minutes long. Note that the duration column is measured in seconds.</b>

- <b>A:SELECT title FROM songs Where mood = 'epic' AND released > 1990 AND duration < 240 ; </b>

<br/>
<img src="https://i.imgur.com/0n3BGI3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<h2>5.Playlist maker</h2>

- <b>Step1 - We've created a database of songs and artists, and you'll make playlists from them in this challenge. In this first step, select the title of all the songs by the artist named 'Queen'. </b>

- <b>A: SELECT title FROM songs Where ARTIST = 'Queen'; </b>

<br/>
<img src="https://i.imgur.com/HJ4AV0b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

- <b>Step 2 - Now you'll make a 'Pop' playlist. In preparation, select the name of all of the artists from the 'Pop' genre. </b>

- <b> A:SELECT name FROM artists WHERE genre = 'Pop' ; </b>

- <b>Step 3 - To finish creating the 'Pop' playlist, add another query that will select the title of all the songs from the 'Pop' artists. It should use IN on a nested subquery that's based on your previous query.</b>

<br/>
<img src="https://i.imgur.com/aR7vgKe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


<h2>6.Gradebook</h2>

- <b> Step 1 - We've created a database to track student grades, with their name, number grade, and what percent of activities they've completed. In this first step, select all of the rows, and display the name, number_grade, and percent_completed, which you can compute by multiplying and rounding the fraction_completed column.</b>


- <b>A: SELECT name, number_grade, ROUND(fraction_completed * 100) AS percent_completed 
 FROM student_grades; </b>
 
- <b>Step 2 - Now, this step is a little tricky. The goal is a table that shows how many students have earned which letter_grade. You can output the letter_grade by using CASE with the number_grade column, outputting 'A' for grades > 90, 'B' for grades > 80, 'C' for grades > 70, and 'F' otherwise. Then you can use COUNT with GROUP BY to show the number of students with each of those grades.</b>

- <b>A:  SELECT COUNT(*),
    CASE
        WHEN number_grade > 90 THEN "A"
        WHEN number_grade > 80 THEN "B"
        WHEN number_grade > 70 THEN "C"
        ELSE "F"
    END AS "letter_grade"
FROM student_grades
GROUP BY letter_grade </b>


<br/>
<img src="https://i.imgur.com/DAHBNkd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
