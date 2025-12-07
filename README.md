# Movies Database API Implementation

## API Overview
The MoviesDatabase API provides access to a vast collection of movie titles, allowing developers to query for movies based on release year, genre, and other criteria. It supports sorting and pagination to manage large datasets effectively.

## Version
Version: v1 (Based on RapidAPI MoviesDatabase documentation)

## Available Endpoints
* **/titles**: The primary endpoint to retrieve a list of movie titles. It supports filtering by year, genre, and list type.
* **/titles/{id}**: Retrieves specific details for a single movie using its unique identifier.
* **/titles/random**: Returns a random movie title from the database.

## Request and Response Format
**Request:**
Requests are made via HTTP GET methods (or POST if proxied as done in this app). Headers must include the RapidAPI key and host.
Example URL: `https://moviesdatabase.p.rapidapi.com/titles?year=2022`

**Response:**
The API returns a JSON object containing pagination data and an array of results.
```json
{
  "page": 1,
  "next": "/titles?page=2",
  "entries": 10,
  "results": [
    {
      "id": "tt1234567",
      "titleText": { "text": "Movie Title" },
      "primaryImage": { "url": "[https://image.url](https://image.url)" },
      "releaseYear": { "year": 2022 }
    }
  ]
}