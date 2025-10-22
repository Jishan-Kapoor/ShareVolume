# Assurant Share Data Viewer

## Summary

The Assurant Share Data Viewer is a static web application that provides users with detailed information about the number of outstanding common stock shares for Assurant (AIZ) based on SEC filings. It fetches data directly from the SEC API, processes it to identify maximum and minimum share counts since 2020, and displays this data in a visually appealing format. Moreover, the app allows for dynamic data retrieval for other companies via their CIK.

## Setup

To deploy this application on GitHub Pages, follow these steps:

1. Fork or clone the repository containing the static web app code.
2. Navigate to the repository settings on GitHub.
3. Scroll down to the "GitHub Pages" section.
4. Select the branch you want to publish and the `root` folder as the source.
5. Save the changes. Your site should be available shortly at `https://<username>.github.io/<repository>`.

Ensure all necessary files, including `index.html`, `data.json`, and `uid.txt`, are committed to the repository.

## Usage

### Accessing the Page

- Visit the live site via GitHub Pages at `https://<username>.github.io/<repository>`.

### Query Parameters

- Append `?CIK=<desired CIK>` to the URL to fetch data for a different company. For example: `index.html?CIK=0001018724`.

### Key Features

- **Real-Time Data**: Fetch and display the number of outstanding shares based on SEC filings.
- **Dynamic Company Data**: Use the query parameter to dynamically update the page for different companies without reloading.

## Code Explanation

### Technical Overview

The application consists of a single HTML page (`index.html`) that performs dynamic data fetching and rendering using JavaScript.

- The page fetches JSON data from the SEC endpoint for the specified CIK.
- JavaScript processes this data to identify maximum and minimum outstanding shares since 2020.
- The identified values are displayed in the web page with appropriate IDs for easy identification.

### Key Libraries

- **Vanilla JavaScript**: The application uses native JavaScript features such as `fetch()` for API calls and DOM manipulation.

### Important Algorithms

- **Data Filtering**: The application filters API data to extract shares outstanding data post-2020 and identifies maximum and minimum values among these entries.

## License

This project is licensed under the MIT License. 

Please refer to the LICENSE file for more details.