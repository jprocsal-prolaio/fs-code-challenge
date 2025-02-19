Let's create a simple SQL coding challenge!  We'll use a simplified database schema for a music streaming service.

**Database Schema:**

We have three tables:

*   **Artists:**
    *   `artist_id` (INT, PRIMARY KEY)
    *   `artist_name` (VARCHAR)

*   **Albums:**
    *   `album_id` (INT, PRIMARY KEY)
    *   `album_title` (VARCHAR)
    *   `artist_id` (INT, FOREIGN KEY referencing Artists)

*   **Tracks:**
    *   `track_id` (INT, PRIMARY KEY)
    *   `track_title` (VARCHAR)
    *   `album_id` (INT, FOREIGN KEY referencing Albums)
    *   `duration` (INT, in seconds)

**Challenge: Music Streaming Queries**

Write SQL queries to answer the following questions:

1.  **Find all albums by a specific artist:**  Given an artist name (e.g., "The Beatles"), find all albums by that artist.  Return the album title and album ID.

2.  **Find the longest track:** Find the track with the longest duration. Return the track title, album title, and artist name.

3.  **Find artists with more than X albums:** Given a number X, find all artists who have more than X albums. Return the artist name and the number of albums they have.

4.  **Find all tracks on a specific album:** Given an album title (e.g., "Abbey Road"), find all tracks on that album. Return the track title and duration.

5.  **Find the total duration of an album:** Given an album ID, find the total duration of all tracks on that album. Return the album title and total duration.

6.  **Find artists with tracks longer than Y seconds:** Given a duration Y, find all artists who have at least one track longer than Y seconds.  Return the artist name.

**Example Data (You can create your own for testing):**

**Artists:**

| artist\_id | artist\_name    |
| :--------- | :------------- |
| 1          | The Beatles    |
| 2          | Led Zeppelin |
| 3          | Pink Floyd     |

**Albums:**

| album\_id | album\_title      | artist\_id |
| :--------- | :--------------- | :--------- |
| 1          | Abbey Road       | 1          |
| 2          | Let It Be        | 1          |
| 3          | IV               | 2          |
| 4          | The Dark Side of the Moon | 3          |

**Tracks:**

| track\_id | track\_title      | album\_id | duration |
| :--------- | :--------------- | :--------- | :------- |
| 1          | Come Together    | 1          | 250      |
| 2          | Something        | 1          | 180      |
| 3          | Stairway to Heaven | 3          | 480      |
| 4          | Money            | 4          | 400      |
| 5          | Get Back         | 2          | 170      |


**Bonus Challenge:**

*   **Find artists who have collaborated:**  Assume an artist can be on multiple albums. Find all pairs of artists who have at least one album in common.

This challenge tests your SQL skills, including joins, aggregations, and subqueries.  Try to write efficient and correct queries for each question.  Let me know if you want to discuss solutions or have any other questions.  I can also provide example solutions if you get stuck.
