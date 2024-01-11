Mito-Links is a web page that transforms the current URL's query parameters into a "deep link" format and then redirects to that new URL. It also displays a countdown before the redirection happens.

# How it works
It first creates a URL object from the current window location.
Then it creates a URLSearchParams object from the search parameters of the URL.
It iterates over these search parameters and appends each value to the deeplink string, separated by slashes (/).
It removes the trailing slash from the deeplink string.
It then sets the window location and the href attribute of a link element to the deeplink string, causing the browser to navigate to the new URL.
It selects a countdown element and its container from the DOM.
It starts an interval that decreases the number displayed in the countdown element by 1 every second.

# Usage
To use this file, simply open it in a web browser. The URL of the page should have query parameters in the format ?param1=value1&param2=value2. The script will transform these into the format /value1/value2 and redirect to that URL.

# Example
If you open the page at the URL https://human-edge.github.io/mito-links/?screen=home&param1=foo&param2=bar, the script will redirect to mitoapp://home/foo/bar.

# Note
This script assumes that there is a link element and a countdown element in the DOM. If these elements are not present, the script will throw an error.
