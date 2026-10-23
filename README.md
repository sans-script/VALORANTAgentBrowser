# VALORANT Agent Browser

A fan-made, interactive agent browser inspired by the agent selection screen in **VALORANT**. Built with Next.js, React, and TypeScript, the interface presents playable agents with their portraits, roles, abilities, and agent-specific background gradients.

**Live demo:** https://valorantagents-browser.vercel.app/

![VALORANT Agent Browser preview](https://github.com/user-attachments/assets/7165e340-d6c8-4fca-8ff7-0c01fdfa9089)

## Features

- **Agent browser:** Highlights the selected agent and displays their role and ability information.
- **Circular navigation:** Browse the agent roster using previous/next buttons or the mouse wheel.
- **Scrollable agent strip:** Select agents from a carousel of up to 13 visible icons.
- **Dynamic backgrounds:** The background gradient changes to match the selected agent.
- **Live agent data:** Fetches playable-agent information from the [VALORANT API](https://valorant-api.com/).

## Tech stack

- **Next.js 16** and **React 18**
- **TypeScript**
- **Tailwind CSS**
- **Material UI Icons**
- **VALORANT API** for agent data

## Getting started

### Prerequisites

- Node.js and npm

### Run locally

1. Clone the repository:

   ```bash
   git clone https://github.com/sans-script/valorant-agents-showcase.git
   cd valorant-agents-showcase
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) in your browser.

The app requests agent data from `https://valorant-api.com/v1/agents?isPlayableCharacter=true`, so loading the roster requires an internet connection and the API to be available.

## Project structure

```text
app/                     Next.js app entry point and global styles
components/
  AgentSlider.tsx        Main agent carousel and navigation controls
  AgentInfo.tsx          Selected agent's role and ability information
  SelectedAgent.tsx      Main selected-agent presentation
hooks/
  useAgents.ts           Agent data loading state
  useAgentNavigation.ts  Circular selection and navigation logic
  useMouseWheel.ts       Mouse-wheel navigation handler
lib/
  fetchAgents.ts         VALORANT API request and agent data type
utils/
  gradient.ts            Background gradient utility
fonts/                   Custom VALORANT-inspired fonts
```

## React concepts demonstrated

- **State and effects:** `useState` and `useEffect` manage fetched agent data and selection state.
- **Custom hooks:** Data loading, navigation, and mouse-wheel handling are separated into reusable hooks.
- **Component composition:** The slider, selected-agent view, and agent information panel have distinct responsibilities.
- **Event handling:** Button clicks and mouse-wheel input move through the roster.
- **Dynamic rendering and styling:** Agent data drives the displayed content, selected-item styling, and background gradient.

## Notes

This is an unofficial fan project made for learning and UI experimentation. VALORANT and its associated names, artwork, and other assets belong to their respective owners. This project is not affiliated with or endorsed by Riot Games.
