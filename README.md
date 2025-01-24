# Automating Reddit Posts

This project allows users to interact with the Reddit API to perform the following tasks:

1. **Login with Reddit**: Authenticate via OAuth2.
2. **View Hot Posts**: Fetch and display a list of hot posts from Reddit.
3. **Create a Post**: Dynamically take user input to create a new post in a specified subreddit.

## Features

- **User Authentication**: Authenticate users using Reddit's OAuth2.
- **Dynamic UI**: User-friendly interface for interacting with the Reddit API.
- **Post Management**: View hot posts and create new posts dynamically.

## Prerequisites

Ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v16+ recommended)
- npm (comes with Node.js)

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/Satyam-Mishra-1/RedditPostAutomater
   cd RedditPostAutomater
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and configure the following variables:

   ```env
   CLIENT_ID=your_reddit_client_id
   CLIENT_SECRET=your_reddit_client_secret
   REDIRECT_URI=http://localhost:3000/reddit/callback
   USER_AGENT=your_custom_user_agent
   ```

   - Replace `your_reddit_client_id`, `your_reddit_client_secret`, and `your_custom_user_agent` with your Reddit API app credentials.

4. Start the server:
   ```bash
   node index.js
   ```

5. Open the app in your browser:
   ```
   http://localhost:3000
   ```

## Project Structure

```
.
├── public
│   └── index.html  # Frontend interface
├── index.js         # Backend logic
├── package.json     # Node.js dependencies
├── .env             # Environment variables
└── README.md        # Project documentation
```

## How to Use

### Login with Reddit
1. Click the **Login with Reddit** button on the homepage.
2. Authorize the app using your Reddit credentials.

### View Hot Posts
1. Click the **Get Hot Posts** button.
2. The app will fetch and display a list of hot posts from Reddit.

### Create a Post
1. Click the **Create a Post** button to display the form.
2. Enter the required details:
   - Subreddit name (e.g., `developer`)
   - Title of the post
   - Content of the post
3. Submit the form to create the post.
4. The app will display the created post's response.

## Dependencies

- [Express](https://expressjs.com/): Web framework for Node.js.
- [dotenv](https://www.npmjs.com/package/dotenv): Load environment variables from `.env` file.
- [request-promise](https://www.npmjs.com/package/request-promise): Simplified HTTP requests.
- [fs](https://nodejs.org/api/fs.html): File system module to handle token storage.

## Troubleshooting

- **Missing Environment Variables**:
  Ensure all variables (`CLIENT_ID`, `CLIENT_SECRET`, `REDIRECT_URI`, `USER_AGENT`) are correctly set in the `.env` file.

- **Invalid Token**:
  If the token expires, delete `reddit_token.txt` and log in again.

- **404 Error on Endpoints**:
  Ensure the server is running on `http://localhost:3000` and the backend routes are correctly implemented.

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it as needed.

## Acknowledgments

- Reddit API Documentation: [https://www.reddit.com/dev/api/](https://www.reddit.com/dev/api/)
- CodingWithAdo: Inspiration for the project.

---
Feel free to contribute to this project by creating a pull request or submitting issues!

