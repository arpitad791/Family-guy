# Family Guy

A full-stack web app built with Next.js where you can browse Family Guy characters and test your knowledge with a quiz.

## Features

- **Character gallery** – a responsive grid of character avatars on the home page.
- **Character pages** – each character has a page with their occupations, description, images, powers and skills, and famous quotes.
- **Quiz** – answer random multiple-choice questions about the show. Pick an answer to see whether it's correct, then move on to the next question.
- **Built-in API** – the data is served from Next.js API routes that read local JSON files.

## Tech Stack

- [Next.js 13](https://nextjs.org/) (App Router)
- [React 18](https://react.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Framer Motion](https://www.framer.com/motion/)
- [React Icons](https://react-icons.github.io/react-icons/)

## API Endpoints

| Method | Endpoint                  | Description                                          |
| ------ | ------------------------- | ---------------------------------------------------- |
| GET    | `/api/characters`         | List all characters                                  |
| GET    | `/api/characters/[slug]`  | Get one character and their quotes                   |
| GET    | `/api/quiz/random`        | Get the ID of a random quiz question                 |
| GET    | `/api/quiz/[id]`          | Get a quiz question and its answer options           |
| GET    | `/api/quiz/answer/[id]`   | Get the correct answer and the next random question  |

## Project Structure

```
app/
  api/            API routes (characters, quiz)
  characters/     Character detail pages
  quiz/           Quiz pages
  page.jsx        Home page (character gallery)
components/       Reusable UI components
data/             JSON data (characters, quotes, quiz)
lib/              Data-fetching helpers
public/           Static images
utils/            API endpoint config
```

## Getting Started

1. Install dependencies:

   ```bash
   npm install
   ```

2. Point the app at your local API. In `utils/endpoint.js`, use the localhost line:

   ```js
   export const endpoint = 'http://localhost:3000/api/'
   ```

3. Start the development server:

   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Scripts

| Command         | Description                   |
| --------------- | ----------------------------- |
| `npm run dev`   | Start the development server  |
| `npm run build` | Build for production          |
| `npm start`     | Run the production build      |
| `npm run lint`  | Run ESLint                    |
