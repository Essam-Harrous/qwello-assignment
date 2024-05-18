# Cats Rock! Vue.js Assignment

## Project Overview

This project is a simple Vue 3 with Typescript application that displays a background image of nice Cat and card with some text and two buttons overlay it for user interaction.

The user can agree or disagree with the statement "Cats Rock!" and its description by clicking the respective buttons. Based on the user's choice, the displayed message changes with a smooth fade-in and fade-out transition effect.

## Technologies Used

- Vue 3
- TypeScript
- HTML5
- CSS3
- CSS Animations

### Prerequisites

- Node.js (>= 12.x)
- npm (>= 6.x) or yarn (>= 1.x)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/vue-assignment.git
   cd vue-assignment

   ```

2. Install Dependencies
   run `yarn` Or `npm i`

3. Run the Project
   `yarn run dev` or `npm run dev`.

## Project Structure

- src/
  - components/
  - App.vue - Root component
  - main.ts - Entry point for the application

## Extra Questions

### 1. How would you improve page speed load time?

Improving page speed load time can be achieved through several strategies:

a. Optimize Images

- Compress images to reduce their file size without losing quality.
- Lazy load images to load them only when they are in the viewport.

b. Use a Content Delivery Network (CDN)

- Serve static assets like images, CSS, and JavaScript files through a CDN to reduce latency. (it's perfect when serving users around the world)

### 2. If you use Server Side or Client Side rendering, what would be some pros and cons (if any) in your chosen method?

#### Server-Side Rendering (SSR)

Pros:

- Better SEO: Content is rendered on the server and is immediately available to search engine crawlers. (I've used it with next.js before for Tanmia360.org project, because they look for better google rank).

- Improved Performance for First Load: Users see the content faster on the initial load, especially beneficial for slower connections.

Cons:

- Higher Server Load: The server needs to render the HTML for each request.
- Reduced Interactivity: Initial interactivity might be slower since JavaScript needs to hydrate the application after the initial HTML is loaded.

### Client-Side Rendering (CSR)

Pros:

- Reduced Server Load: The server only needs to serve static assets, reducing the computational load on the server.
- Simpler Deployment: Static files can be served from a CDN.
- Rich Interactivity

Cons:

- Initial Load Time: The browser needs to download and execute JavaScript before rendering the content, which can increase the time to interact (TTI).
- SEO Challenges: Search engines might have difficulty indexing client-rendered content unless proper server-side pre-rendering techniques are used.
- Performance on Slow Devices.

#### Conclusion

The choice between SSR and CSR depends on the specific requirements of the project.

For applications where SEO and initial load performance are critical, SSR is a better choice. like content maker websites and newspapers etc.

For highly interactive applications where subsequent navigation need to be very fast, CSR might be more like Dashboards
