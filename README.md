🛠️ Wikipedia Search App — 

Static Functionality Brief

✅ HTML5 layout with Bootstrap 4.5.2 for responsive styling.
🔍 Search input (#searchInput) inside a centered header with Wiki logo.
⏳ Spinner (#spinner) hidden by default, shown during API calls.
📥 Results container (#searchResults) where search results are injected.
🧩 Uses classes: wiki-logo, search-input, d-none, spinner-border, search-results.

Dynamic Functionality Brief

🔁 1. Event Listener Setup
Inside the event listener, I called the function giveSearchResults() to handle user search actions.
 It checks if the key pressed is Enter, triggering the fetch logic only then.

🌐 2. Fetch API Integration
Within giveSearchResults(), I used the fetch() method to hit the Wiki API using the input value.
 The response was then converted to JSON using .json() for further parsing.

📥 3. Parsing JSON & Accessing Data
After parsing, I observed that the key "search_results" holds an array of result objects.
 This array became the input to createEachSearchResult(search_results).

🔄 4. Looping Through Results
In createEachSearchResult(), I used a for...of loop to iterate over each search result.
 Each result was passed to displaySearchResultOfEach() for rendering.

🧱 5. DOM Creation & Rendering
In displaySearchResultOfEach(), I dynamically created elements:
📌 Title: <a> with class result-title, linked via href, opened with _blank.

🌐 URL: Another <a> with class result-url, also using href and _blank.

📝 Description: <p> with class link-description.

I also added <br> tags for layout spacing. Everything was appended to js_searchResults.

⚠️ 6. Variable link redirection
