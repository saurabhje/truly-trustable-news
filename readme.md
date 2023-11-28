# The Third Front

## Introduction
The Third Front is a web app designed to deliver harmless and humorous satire news posts, offering a refreshing break from mainstream media's fear-centric approach. Our mission is to **present the truth under the veil of satire**.

### Goal
Our goal is to provide the community with a dose of humorous jokes, making news less intimidating and morbid for the average reader.

## Getting Started
### Prerequisites
- List of required software and tools with download/installation links.

### Installation
1. Clone the repository.
2. Navigate to /Frontend and install frontend dependencies using `npm install`.
3. Navigate to /Backend and install backend dependencies using `npm install`.

## Architecture
### Tech Stack
- Vite.js/React.js
- Node.js
- Express
- MongoDB

### Folder Structure
/Truly-Trustable-News
  /Backend
    /src
      /model
        /Categories
        /News
      /methods
        - /News_Operation
        - /Category Operation
      index.js
      .env

  /Frontend
    /images
      - (Store images used in documentation)
    - CONTRIBUTING.md
    - API_DOCUMENTATION.md
    - USAGE_GUIDE.md
  /scripts
    - (Scripts for automation or other purposes)
  /data
    - (Data files, if any)
  /.gitignore
  /README.md


## Configuration
### Environment Variables
Set up environment variables:
- **For /Frontend:**
  1. `VITE_base_url`: Your backend API URL (e.g., 'http://localhost:port').
- **For /Backend:**
  1. `MONGODB_URI`: MongoDB cluster URI.
  2. `PASSWORD`: Password for CRUD operations (set up during password setup).

## Development
### Running the App Locally
1. To run the Frontend locally, use `npm run dev`.
2. To run the backend locally, use `npm run dev`.

### Testing
Unit testing is performed for data fetching and authorization using the built-in **vitest** feature of Vite.js, similar to Jest testing library.

## API Documentation
### Endpoints
- All the get requests
get('/admin', news_operations.allNews);
get('/', news_operations.allNewsHome);
get('/news/:id', news_operations.getNews);
get('/categories',category_Operations.allCategories);
get('/category/:id', category_Operations.category_news_list);
get('/edit/:id', news_operations.edit_news_get);

- All the POST requests
post('/create-news',news_operations.create_News_post);
post('/delete/:id',news_operations.delete_news);
post('/edit/:id', news_operations.edit_News_post);

### Authentication
The app uses a simple sessionStorage-based authentication since there is only one user performing admin operations.

## Database
### Database Schema
Two main schemas are used:
1. NewsSchema
2. CategorySchema

## Deployment
### Deployment Process
The full-stack web app is deployed on Vercel.

**Deploying the Backend:**
1. Configure vercel.json in the root folder of Backend.
2. Create a new project on vercel.com from your GitHub repo, choosing Backend as the source directory.
3. Set up environment variables for the Backend (MongoDB URI and password) and click on deploy.

**Deploying the Frontend:**
1. Choose the GitHub repo, and select Frontend as the source directory.
2. Set the environment variable for the frontend (VITE_base_url is the URL obtained after deploying the backend).

## Additional Resources
### Links to Documentation
[Why Vite.js][1]
[React.js][2]
[Deploying on Vercel][3]

[1]: https://vitejs.dev/guide/why
[2]: https://react.dev/learn
[3]: https://vercel.com/docs/frameworks/vite


### Contact Information
[Mail us][jeiolsatszs@gmail.com]

## Conclusion
### Acknowledgments
Used ReactQuill for rich text and Vitest for unit testing.

