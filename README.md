# Gen Z Slang Dictionary

This project is a simple, single-file web application that functions as a dictionary for common Gen Z slang terms. It allows users to quickly search for terms and their definitions, making it easier to understand the ever-evolving language of the younger generation.

## How to Use

1.  **Save the file:** Save the provided `index.html` content to a file named `index.html` on your computer.
2.  **Open in browser:** Open the `index.html` file using any modern web browser (e.g., Chrome, Firefox, Edge, Safari).
3.  **Search:** Use the search bar at the top of the page to type in slang terms or keywords. The dictionary will instantly filter and display matching terms and their definitions as you type. If the search bar is empty, all terms will be displayed.

## Code Explanation

The application is built using only HTML and vanilla JavaScript within a single `index.html` file, ensuring maximum simplicity and portability.

*   **HTML Structure:**
    *   A main `div` container holds the title, search input, and results area.
    *   An `input` element (`id="searchInput"`) serves as the search bar.
    *   A `div` (`id="results"`) is where the dictionary terms and their definitions are dynamically inserted.
*   **CSS Styling:**
    *   Minimalist CSS is embedded directly in the `<style>` tags to provide a clean, modern, and user-friendly interface. It includes basic typography, layout adjustments for readability, and subtle hover effects for term items.
*   **JavaScript Logic:**
    *   **Data:** A JavaScript array named `slangData` stores the dictionary entries. Each entry is an object with `term` and `definition` properties.
    *   **`searchInput` and `resultsDiv`:** DOM elements are retrieved for the search input and the results display area.
    *   **`displayResults(termsToDisplay)` function:** This function takes an array of term objects and dynamically generates HTML `div` elements for each term, displaying its header and definition within the `resultsDiv`. It also handles the case where no results are found.
    *   **`searchDictionary()` function:** This is the core search logic. It retrieves the current value from the search input, converts it to lowercase, and then filters the `slangData` array. It searches for matches in both the `term` and `definition` fields.
    *   **Event Listeners:**
        *   `DOMContentLoaded`: When the page loads, `displayResults(slangData)` is called to show all dictionary terms initially.
        *   `input` on `searchInput`: As the user types in the search bar, the `searchDictionary()` function is called repeatedly to provide a live-filtering experience.

## License

This project is licensed under the MIT License.