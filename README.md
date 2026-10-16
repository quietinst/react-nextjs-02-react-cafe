# 02 — React Café

🔗 [Live demo](https://react-nextjs-02-react-cafe.vercel.app)

A feedback widget for a coffee shop. Visitors rate the service with one of three
options — good, neutral, or bad — and instantly see the statistics.

My first React + TypeScript app: component composition, state, props, typed
handlers, and conditional rendering.

## Features

- Three vote options (Good, Neutral, Bad) with a Reset button
- Live statistics: votes per option, total votes, and the percentage of positive
  feedback
- Reset button appears only when there is at least one vote
- A "No feedback yet" message while there are no votes

## Tech stack

- React + TypeScript
- Vite
- CSS Modules
- modern-normalize

## Project structure

```text
src/
├── components/
│   ├── App/
│   ├── CafeInfo/
│   ├── VoteOptions/
│   ├── VoteStats/
│   └── Notification/
├── types/
│   └── votes.ts
└── main.tsx
```

Each component folder contains the component (`.tsx`) and its styles
(`.module.css`). Types shared between several components live in
`src/types/votes.ts`.

## Getting started

```bash
npm install
npm run dev       # local dev server
npm run build     # type-check + production build
npm run preview   # preview the production build
```

## Concepts covered

| Concept                    | Where                                            |
| -------------------------- | ------------------------------------------------ |
| Component composition      | `App` renders all other components               |
| State (`useState`)         | `votes` object in `App`                          |
| Props and typed interfaces | `VoteOptionsProps`, `VoteStatsProps`             |
| Derived values             | `totalVotes`, `positiveRate` computed from state |
| Conditional rendering      | `VoteStats` vs. `Notification`, the Reset button |
