---
description: Enter comment mode to leave feedback on specific parts of Claude's last response
disable-model-invocation: true
---

Run `highlight-state mode-on` using the Bash tool.

Then tell the user, briefly (2-3 sentences): comment mode is now active. They should select/highlight any part of your previous response with the mouse (it copies to the clipboard automatically), then just type their comment as a normal message — no slash command needed. Each one gets confirmed immediately, and they can repeat this for as many parts as they want. When they're done, they run `/highlight:submit`.

Do not do anything else in this turn.
