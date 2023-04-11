## What is SSR and CSR?

### SSR: 

Server-Side Rendering - rendering a client-side or universal app to HTML on the server.
1. Server-side rendering (SSR) is the process of generating HTML, CSS, and JavaScript on the server-side and sending a fully rendered page to the client-side, instead of sending just the bare-bones markup and loading everything else on the client-side using JavaScript.
2. With SSR, when a user requests a web page, the server generates the HTML content and sends it to the client, along with the necessary CSS and JavaScript.
3. The client can then display the page without having to wait for additional requests to the server or for JavaScript to execute, resulting in faster loading times and better user experience.
4. SSR is particularly useful for websites with dynamic content that changes frequently or for websites that want to improve their SEO (search engine optimization) since search engines can crawl and index the fully rendered pages.

### CSR:

Client-Side Rendering - rendering an app in a browser, generally using the DOM.
1. Client-side rendering (CSR) is the process of rendering web pages on the client-side, typically using JavaScript, instead of generating the full HTML, CSS, and JavaScript on the server-side.
2. With CSR, when a user requests a web page, the server sends only the basic HTML and JavaScript required to display the page. 
3. Then, the client-side JavaScript code is responsible for fetching the data from the server and rendering the page on the client-side.
4. This approach allows for more interactivity and faster page load times, since the initial page load only requires a minimal amount of data to be transferred from the server, and subsequent interactions with the page can be handled locally without requiring a round trip to the server.
5. However, CSR can also have some downsides, such as slower initial load times if the JavaScript code is large or if the client's device has limited processing power, and potentially lower search engine optimization (SEO) since search engines may not be able to index the content of the page as effectively.
