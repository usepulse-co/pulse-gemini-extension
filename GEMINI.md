# Pulse Data Rooms

The `pulse` tools read and change the signed-in user's own Pulse workspace: their document library, the share links they created, and how the people they shared with engaged. Nothing here reaches another workspace, and no tool sends a message to anyone.

- Search before answering questions about what a document says (`pulse_search_documents`, then `pulse_get_document_page` for the exact page).
- Engagement questions (who opened a link, what they read, how warm a contact is) go to the `pulse_get_*` contact and analytics tools.
- `pulse_ask_perry` asks Pulse's own analyst a question and returns a cited answer. It does not change anything.
- Deleting, revoking a viewer, and changes that take away access people already have return a `pending_confirmation` first. Show it to the user and call `pulse_confirm_action` only after they approve.
- Other changes (creating links and folders, moving and renaming, changing link settings that widen access) run as soon as they are called, so make sure the user asked for them.
- Uploads are three steps: `pulse_request_upload`, a PUT of the file bytes to the returned URL, then `pulse_complete_upload`.
