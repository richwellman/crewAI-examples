# Comprehensive Overview of the Netflix Table

The Netflix table is a structured data representation of content available on the platform, detailing attributes such as show type, title, director, cast, and more.

## Columns Description

| Column Name        | Data Type    | Description                                                                                       |
|--------------------|--------------|---------------------------------------------------------------------------------------------------|
| show_id            | varchar      | A unique identifier for each show or movie in the Netflix library.                               |
| type               | varchar      | The format of the content, indicating whether it is a movie or a TV show.                        |
| title              | varchar      | The title of the show or movie.                                                                   |
| director           | varchar      | The name of the director associated with the show or movie.                                       |
| cast               | varchar      | The list of actors or performers featured in the show or movie.                                   |
| country            | varchar      | The country where the show or movie was produced or made available.                               |
| date_added         | varchar      | The date the show or movie was added to the Netflix library.                                      |
| release_year       | int64        | The year the show or movie was originally released.                                              |
| rating             | varchar      | The content rating, providing an indication of the target audience suitability.                   |
| duration           | varchar      | The length of the show or movie, typically expressed in minutes or termed as seasons for TV shows. |
| listed_in          | varchar      | Genre categories that the show or movie falls under.                                             |
| description        | varchar      | A brief summary or synopsis of the show or movie, outlining key themes and plot details.          |