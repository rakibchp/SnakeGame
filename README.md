# Little Arcade — Snake

A responsive take on the classic Snake game, built with Next.js, React, and
Tailwind CSS. Guide the snake around the board, collect fruit, and see how high
you can score without running into a wall or your own tail.

## Features

- **Responsive board:** The 20 × 20 game board scales to fit phones, tablets,
  laptops, and desktop displays.
- **Keyboard controls:** Steer with the arrow keys or **WASD**.
- **Touch controls:** Use the on-screen direction pad on touch-oriented devices.
- **Score and growth:** Each fruit adds 10 points and one segment to the snake.
- **Increasing challenge:** The snake speeds up as your score increases, up to a
  maximum speed.
- **Pause and restart:** Pause, resume, or start a fresh round at any time.
- **Live stats:** Keep track of your current score, session best, and snake
  length.
- **Accessible details:** Controls have labels, status and score updates are
  announced, and reduced-motion preferences are respected.
- **Arcade-inspired interface:** A dark, high-contrast design with animated
  fruit and responsive layouts.

## Getting started

### Requirements

- Node.js compatible with Next.js 16
- npm

### Install and run locally

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Production

Build and run the production version:

```bash
npm run build
npm run start
```

By default, the production server runs at [http://localhost:3000](http://localhost:3000).

## How to play

1. Select **Let’s play** or **Start game**, or press a direction key to begin.
2. Guide the snake toward the fruit.
3. Each fruit earns **10 points** and makes the snake longer.
4. Avoid the edges of the board and the snake’s body.
5. Keep collecting fruit to increase your score. The snake gets faster as your
   score rises.

The board is 20 × 20 cells. A round ends when the snake hits a wall or itself.
Filling every cell on the board wins the round.

## Controls

| Action | Keyboard | Touch |
| --- | --- | --- |
| Move | Arrow keys or **W**, **A**, **S**, **D** | Tap a direction button |
| Start, pause, or resume | **Space** or **Enter** | Use the game action button |
| Restart | **R** | Use **Play again** after a round ends |

The snake cannot immediately reverse into the direction it is currently moving.

## Scoring and speed

- Each fruit is worth **10 points**.
- The snake starts at its initial speed and gets faster for every 50 points.
- Speed increases stop at the game's maximum speed.
- The personal-best score lasts for the current page session. It resets when
  the page is reloaded; it is not saved to browser storage.

## Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Next.js development server. |
| `npm run build` | Create an optimized production build. |
| `npm run start` | Serve the production build. Run `npm run build` first. |
| `npm run lint` | Check the project with ESLint. |

## Project structure

```text
app/
  globals.css   Global styles, Tailwind import, and responsive game styling
  layout.tsx    Root layout, fonts, and page metadata
  page.tsx      Snake game UI, state, controls, and game loop
public/         Static assets
```

## Technology

- [Next.js](https://nextjs.org/) 16 with the App Router
- [React](https://react.dev/) 19
- [Tailwind CSS](https://tailwindcss.com/) 4
- [TypeScript](https://www.typescriptlang.org/)
