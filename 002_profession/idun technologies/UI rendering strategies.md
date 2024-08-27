#core/softwareengineering #core/webdevelopment

- **Static website**: These are pre-built web pages, often written purely in HTML, CSS, and JavaScript, that are delivered to the client without any changes. They are fast and secure but aren’t dynamic and can’t interact with databases in real-time.

- **Multi-page apps (MPA)**: Traditional web applications that reload the entire page and render HTML on the server side each time the user navigates to a different part of the website. This can lead to slower transitions between pages.

- **Single-page app (SPA)**: A web application that fits on a single web page with the goal of providing a more fluid user experience. The page doesn’t need to reload during use and typically communicates with the web server in the background (AJAX) to update and modify the page.

- **Server-side rendering with hydration (SSR)**: This is a technique where the server sends a fully rendered page to the client. The client’s JavaScript bundle can then “hydrate” this pre-rendered page, allowing it to take over and enable SPA-style interactions.

- **Static site generation with hydration (SSG)**: The HTML is pre-rendered at build time and can be served directly to the client. JavaScript “hydration” can then add more complex interactions on the client side. This strategy is often used in modern frontend frameworks like Next.js.

- **Incremental static regeneration (ISR)**: A hybrid rendering method where static pages are generated at build time and revalidated or updated incrementally after deployment. This approach provides the benefits of static rendering while allowing for updates when the underlying data changes.

- **Partial hydration**: A technique used in SSR/SSG where not all components are fully hydrated on the client side. This can improve performance by reducing the amount of JavaScript that needs to be executed.

- **Islands Architecture**: A modern approach that involves combining static rendering and client-side interactions, dividing a UI into separate “islands” of interactivity. Some parts of the page are fully static, while others (“islands”) are richly interactive and handled client-side.

- **Streaming Server-Side Rendering (Streaming SSR)**: An enhancement of SSR where the HTML response is streamed to the client and the browser can start receiving and parsing the HTML even before the entire page has been generated on the server. This can lead to faster Time To First Byte (TTFB) and perceived loading times.

- **Resumability:** In the context of e.g. the Qwik JavaScript framework, resumability refers to the ability to pause execution on the server and resume it on the client without needing to replay or download all of the application logic. This allows the app to be fully serialised as HTML, contributing to an improved performance and user experience by reducing the amount of JavaScript that needs to be transferred and parsed.