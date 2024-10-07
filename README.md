# React Drag-and-Drop Columns and Items Project

This project implements a drag-and-drop interface using React and `react-beautiful-dnd` where users can move items between columns and reorder the columns themselves.

<a href="https://dragn-drop-next-app.vercel.app/" target="_blank"><img src="https://dragn-drop-next-app.vercel.app/image-1.png" alt="Description of image" /></a>

## Features

- **Drag and Drop Items**: Users can drag and drop items within a column or move them to other columns.
- **Reorder Columns**: Users can reorder columns by dragging and dropping them.
- **Empty Columns Handling**: Columns without items are also droppable, ensuring a smooth user experience.

## Prerequisites

Before setting up the project, make sure you have the following installed on your local machine:

- **Node.js**: Download and install Node.js from [nodejs.org](https://nodejs.org).
- **npm**: Node Package Manager is installed automatically with Node.js.

## Installation

1. **Clone the Repository**

   Clone the project to your local machine using the following command:

   ```bash
   git clone https://github.com/imarjunshrma/DragnDropNextApp.git
   ```

2. **Navigate to the Project Directory**

   ```bash
   cd your-repo-name
   ```

3. **Install Dependencies**

   Install all the required dependencies for the project:

   ```bash
   npm install
   ```

## Configuration

To ensure that the drag-and-drop functionality works correctly, **React's strict mode must be disabled**. You can disable it by modifying the `next.config.js` file in your Next.js project.

1. Open the `next.config.js` file.
2. Add the following configuration:

   ```javascript
   const nextConfig = {
     reactStrictMode: false,
   };

   module.exports = nextConfig;
   ```

**Important**: The project will only function correctly if `reactStrictMode` is set to `false`. React's strict mode is known to cause issues with the drag-and-drop functionality by performing double rendering of components in development mode, which interferes with the way state updates work in `react-beautiful-dnd`.

## Usage

Once you have installed the dependencies and disabled strict mode, you can start the project locally with:

```bash
npm run dev
```

Then open [http://localhost:3000](http://localhost:3000) in your browser to view the drag-and-drop application.

## How It Works

- The app allows users to drag items between columns and reorder both items and columns.
- The components are rendered dynamically based on the structure of the data.
- **`onDragEnd`**: This function handles both column reordering and item movement within or between columns. The data structure is updated when a drag-and-drop action is completed.

## Project Structure

- **`components/`**: Contains the reusable UI components for the app.
- **`utils/`**: Includes utility functions (if any).
- **`pages/`**: Main app entry point.
- **`next.config.js`**: Next.js configuration file where strict mode is disabled.

