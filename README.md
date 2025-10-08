# SaveMyGPT Documentation

## 1. Overview
SaveMyGPT is a Chrome extension that lets you capture ChatGPT conversations locally, browse them in a polished popup, and reuse curated prompts. Everything runs on-device; no chat history or prompt data is sent to external servers.

## 2. Features
- **One-click capture**: A floating `SaveMyGPT It!` button on ChatGPT.com saves the current selection or composer text.
- **Context menu capture**: Right-click on ChatGPT pages to save the full conversation or a highlighted snippet.
- **Memories dashboard**: Search, expand, copy, paste, delete, export, or import stored conversations.
- **Prompt Library**: Browse the bundled prompt collection, search by use case, and paste instantly into ChatGPT.
- **Options page**: Toggle autosave, adjust storage limits, and choose which roles (user/assistant) to capture.

## 3. Installation
1. Download or clone the SaveMyGPT repository.
2. Open `chrome://extensions`, enable Developer Mode.
3. Click `Load unpacked` and select the project folder.
4. Pin the SaveMyGPT icon from the Chrome toolbar if desired.

## 4. Using SaveMyGPT
### Capture Workflow
1. Open a conversation on ChatGPT.
2. Highlight text (optional) or type into the composer.
3. Click `SaveMyGPT It!` or use the `Save with SaveMyGPT` context menu options.

### Managing Memories
- Open the toolbar popup to view saved memories.
- Use the search bar to filter by keywords or tags (e.g., `#prompt`).
- `Paste`: Inserts the memory into the active ChatGPT tab.
- `Copy`: Copies the snippet to the clipboard.
- `Delete`: Removes the memory from local storage.
- `Export`: Downloads all memories as JSON.
- `Import`: Merges memories from a JSON file.
- `Clear All`: Permanently removes every stored memory.

### Prompt Library
- Switch to the `Prompt Library` tab in the popup.
- Search by keyword or browse the list of packed prompts.
- Click `Paste` to drop the prompt into ChatGPT.

## 5. Options
Access the options page via the popup footer or `chrome://extensions` > Details > Extension options.
- **Autosave**: Automatically capture when a manual scrape is triggered.
- **Max memories**: Set the maximum number of stored items (oldest entries are trimmed as new ones arrive).
- **Capture roles**: Choose whether to save user messages, assistant responses, or both.

## 6. Permissions
SaveMyGPT requests the following permissions:
- `storage` — store memories and settings locally.
- `activeTab` / `tabs` — interact with the current ChatGPT tab when saving or pasting.
- `scripting` — inject the content script on demand and paste into the ChatGPT composer.
- `contextMenus` — provide right-click capture actions.

## 7. Privacy & Security
- All data stays in `chrome.storage.local`; nothing is transmitted externally.
- The prompt library (prompts.json) is bundled with the extension.
- See `index.html` for a full security and privacy statement.

## 8. Troubleshooting
| Issue | Fix |
|-------|-----|
| Floating button missing | Refresh the ChatGPT tab. Ensure the extension is enabled. |
| Paste shows "Open chat tab" | Make sure the ChatGPT tab is active and focused when pressing Paste. |
| Memories not saving | Check options to confirm role capture is enabled and storage quota is not exceeded. |
| Prompt Library empty | Reload the extension; ensure `prompts.json` is present in the extension package. |

## 9. Updating
1. Pull the latest changes or replace the extension folder contents.
2. In `chrome://extensions`, click the reload icon for SaveMyGPT.
3. Verify the version and features in the popup.

## 10. Support
For questions, feature requests, or security concerns, email `support@savemygpt.app`.
