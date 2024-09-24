# Stay Productive

Stay Productive is a simple yet effective Chrome extension designed to help users block distracting websites, promoting better focus and productivity. The extension provides the ability to temporarily or fully block certain websites for an entire day.

## Features

- Block websites temporarily or for a full day.
- Timer to track how long before a site gets completely blocked.
- Prevents access to already blocked sites with an option to close the tab.
- Custom error messages for invalid URLs (e.g., Chrome internal pages).

## How It Works

1. **Popup UI**: Displays the current website and provides a button to block it.
2. **Content Script**: Injects a timer on the webpage, displaying the countdown to when the site will be blocked.
3. **Background Script**: Handles blocking, manages URL storage, and closes tabs once the timer finishes.

## Technologies Used

- **JavaScript**: Core functionality of the extension.
- **HTML & CSS**: For the popup and injected timer UI.
- **Chrome Extensions API**: 
  - `chrome.tabs`: Retrieves and manipulates the active tab.
  - `chrome.storage`: Saves and retrieves blocked URLs.
  - `chrome.runtime`: Handles communication between background and content scripts.

## How to Install

1. Clone this repository:
    ```bash
    git clone https://github.com/Amitabh0954/chrome-Extension.git
    ```
2. Open Chrome and navigate to `chrome://extensions/`.
3. Enable **Developer Mode**.
4. Click **Load unpacked** and select the cloned repository folder.
5. The extension will appear in your browser toolbar.

## Usage

1. Open any website you want to block.
2. Click on the Stay Productive extension in the toolbar.
3. Click the **Block** button.
4. A timer will appear on the page. Once the timer finishes, the page will be blocked, and the tab will be closed.
5. You can block multiple websites, and they will remain blocked for the day.

## Project Structure

- `manifest.json`: Describes the extension's properties and permissions.
- `popup.html`: The UI for the extension's popup.
- `popup.js`: Logic for displaying the current URL and initiating the block process.
- `contentScript.js`: Injects the countdown timer into the page.
- `background.js`: Handles storing blocked websites and sending messages to other scripts.
- `styles/`: Contains CSS styles for the popup and injected timer UI.

## Why I Built This

As someone who often struggles with staying focused, I built this project to help users avoid distractions and maximize productivity. Unlike more complex projects, this Chrome extension provides a simple, quick solution to block distracting websites in a user-friendly manner.

## Future Enhancements

- Add customization for blocking durations.
- Display all blocked sites with an option to unblock them.
- Integrate notifications when the block period ends.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
