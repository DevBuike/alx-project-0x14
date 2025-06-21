# alx-project-0x14  
## API Overview  
Collection of information for movies, tv-shows, actors. Includes youtube trailer url, awards, full biography, and many other usefull informations. This api provides complete and updated data for movies, series and episodes.  

## API Version  
I'm using the V1 of the API.  

## Available Endpoints  
  - `GET /titles/search/title/{title}` – Search for movies or shows by title
  - `GET /titles/{id}` – Get detailed info about a specific title
  - `GET /actors/{id}` – Retrieve biography and filmography of an actor
  - `GET /titles/{id}/trailer` – Get the YouTube trailer URL for a title
  - `GET /titles/{id}/awards` – Fetch awards and nominations for a title  

## Request and Response Format  
**Request Example:**
```http```
GET /titles/search/title/Inception
Host: moviesdatabase.p.rapidapi.com
x-rapidapi-key: YOUR_API_KEY
x-rapidapi-host: moviesdatabase.p.rapidapi.com  

**Response Example**
{
  "results": [
    {
      "id": "tt1375666",
      "title": "Inception",
      "year": 2010,
      "genres": ["Action", "Sci-Fi"],
      "trailer": "https://youtube.com/watch?v=YoHD9XEInc0"
    }
  ]
}

## Authentication  
All requests require authentication via RapidAPI headers:
- x-rapidapi-key: Your personal API key
- x-rapidapi-host: moviesdatabase.p.rapidapi.com

## Error Handling  
Common error responses include:
  - 401 Unauthorized – Missing or invalid API key
  - 404 Not Found – Resource not found (e.g., invalid ID)
  - 429 Too Many Requests – Rate limit exceeded

## Usage Limits and Best Practices  
  - Rate Limit: The API may enforce request limits depending on your subscription tier.
  - Best Practices:
    - Cache frequent requests to reduce load
    - Handle errors and retries with exponential backoff
    - Avoid hardcoding your API key in public repositories

