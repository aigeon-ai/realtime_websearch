```markdown
# Aigeon AI Real-Time Web Search

Aigeon AI Real-Time Web Search is a Python-based server application designed to provide real-time organic search results from across the web. Leveraging advanced search parameters and geo-targeting, this application supports Google Search operators and offers both single and batch search capabilities.

## Features Overview

- **Real-Time Search:** Fetches organic search results in real-time using advanced search parameters.
- **Geo-Targeting:** Supports city-level geo-targeting to simulate searches from specific locations.
- **Google Search Operators:** Utilizes Google Advanced Search operators such as `inurl:`, `site:`, `intitle:`, etc.
- **Batch Processing:** Capable of handling up to 100 search queries in a single request for efficient batch processing.

## Main Features and Functionality

1. **Real-Time Organic Search:**
   - The application provides real-time search results by interfacing with a third-party API.
   - Supports various Google Search parameters, including language (`hl`), region (`gl`), and advanced search options (`tbs`).

2. **Geo-Targeting and Localization:**
   - Allows searches to be conducted from specific locations, enhancing the relevance of search results based on geographic context.
   - Users can specify the location at the city level to mimic real user searches.

3. **Batch Search Capability:**
   - Offers a high-performance endpoint for processing multiple search queries simultaneously.
   - Designed to handle up to 100 queries in a single request, making it suitable for applications requiring bulk data retrieval.

## API Endpoints or Main Functions Description

### `search`

- **Description:** Retrieves real-time organic search results with support for various Google Search parameters and geo-targeting.
- **Parameters:**
  - `q` (str): Search query.
  - `num` (Union[int, float], optional): Maximum number of results to return.
  - `start` (Union[int, float], optional): Number of results to skip (for pagination).
  - `gl` (str, optional): Country/region for the query.
  - `hl` (str, optional): Language for the search.
  - `tbs` (str, optional): Advanced search parameters.
  - `location` (str, optional): Origin location of the search.
  - `nfpr` (str, optional): Exclude results of auto-corrected queries.
- **Returns:** A dictionary containing the search results.

### `batch_search`

- **Description:** Provides a high-speed endpoint for retrieving organic search results for up to 100 queries in a single request.
- **Parameters:** None specified in the function signature.
- **Returns:** A dictionary containing the batch search results.

## Usage

The application is designed to be run as a server using the `FastMCP` framework, which facilitates communication over standard input/output. The primary functions, `search` and `batch_search`, are exposed as tools within this framework, allowing for seamless integration and execution.

---

This README provides a comprehensive overview of the Aigeon AI Real-Time Web Search application, highlighting its capabilities and usage. For further details or to contribute, please refer to the repository documentation and codebase.
```
