# YouTube Unblocker

A lightweight, browser-like unblocker for watching YouTube videos built with pure vanilla HTML, CSS, and JavaScript.

## Features

- **Pure Vanilla Implementation**: No frameworks or libraries - just HTML, CSS, and JavaScript
- **Browser-like Interface**: Complete with tabs, address bar, and content area
- **Catppuccin Mocha Theme**: Dark theme with the Catppuccin Mocha color palette
- **Tab Management**: Create new tabs, switch between tabs, and close tabs
- **YouTube Embedding**: Enter a YouTube URL and watch videos directly in the interface
- **Responsive Design**: Adapts to different screen sizes
- **Fullscreen Mode**: Toggle fullscreen viewing for a better experience
- **Privacy-Enhanced**: Uses YouTube's no-cookie embed URLs

## How to Use

1. Open `index.html` in any modern web browser
2. Enter a YouTube URL in the address bar and press Enter
3. The app extracts the video ID and embeds the video
4. Create multiple tabs by clicking the + button
5. Switch between tabs by clicking on them
6. Close tabs by clicking the × button
7. Toggle fullscreen mode with the expand/collapse button

## Data URL

You can use this app in a data URL:

`data:text/html,%3C!DOCTYPE%20html%3E%0A%3Chtml%20lang%3D%22en%22%3E%0A%3Chead%3E%0A%20%20%3Cmeta%20charset%3D%22UTF-8%22%3E%0A%20%20%3Cmeta%20name%3D%22viewport%22%20content%3D%22width%3Ddevice-width%2C%20initial-scale%3D1.0%22%3E%0A%20%20%3Ctitle%3EClassroom%3C%2Ftitle%3E%0A%20%20%3Cscript%3E%0A%20%20%20%20document.addEventListener(%22DOMContentLoaded%22%2C%20()%20%3D%3E%20%7B%0A%20%20%20%20%20%20const%20main%20%3D%20%22https%3A%2F%2Fraw.githubusercontent.com%2Fsmartfoloo%2Fyoutube-unblocker%2Frefs%2Fheads%2Fmain%2Findex.html%22%3B%0A%20%20%20%20%20%20const%20fallback%20%3D%20%22https%3A%2F%2Fcdn.jsdelivr.net%2Fgh%2Fsmartfoloo%2Fyoutube-unblocker%2Findex.html%22%3B%0A%0A%20%20%20%20%20%20fetch(main)%0A%20%20%20%20%20%20%20%20.then(response%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20if%20(!response.ok)%20throw%20new%20Error(%22Primary%20URL%20failed%22)%3B%0A%20%20%20%20%20%20%20%20%20%20return%20response.text()%3B%0A%20%20%20%20%20%20%20%20%7D)%0A%20%20%20%20%20%20%20%20.catch(()%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20return%20fetch(fallback).then(response%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20if%20(!response.ok)%20throw%20new%20Error(%22Fallback%20URL%20failed%22)%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20return%20response.text()%3B%0A%20%20%20%20%20%20%20%20%20%20%7D)%3B%0A%20%20%20%20%20%20%20%20%7D)%0A%20%20%20%20%20%20%20%20.then(html%20%3D%3E%20%7B%0A%20%20%20%20%20%20%20%20%20%20document.open()%3B%0A%20%20%20%20%20%20%20%20%20%20document.write(html)%3B%0A%20%20%20%20%20%20%20%20%20%20document.close()%3B%0A%20%20%20%20%20%20%20%20%7D)%3B%0A%20%20%20%20%7D)%3B%0A%20%20%3C%2Fscript%3E%0A%3C%2Fhead%3E%0A%3C%2Fhtml%3E%0A%0A%0A`