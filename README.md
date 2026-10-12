For future addon packages, I’ll include usage instructions inside the ZIP. This ZIP remains unchanged.
Create README.md in your repository and paste the following:
Accolades Buy-All
Author: Soliserio
Version: 1.0.2
Requires: Windower 4
Buys Prize Powder from Urbiolaine in Southern San d’Oria using Unity accolades, not Sparks.
Supports single-item and bulk purchases. Bulk quantities are limited by available accolades, the remaining weekly spending allowance, and Inventory capacity.
Installation
Extract the ZIP into your Windower folder, preserving this structure:
Windower/
  addons/
    accolades/
      accolades.lua
      prizepowder.lua
Load the addon in game chat:
//lua load accolades
Both acco and accolades work as command names.
Buying Prize Powder
Stand idle and disengaged within six yalms of Urbiolaine, with other menus closed.
Test one Prize Powder first—it costs 10 Unity accolades:
//acco buy prize powder
Buy as many as current limits permit:
//acco buyall prize powder
buyall is one word. prize powder is two words.
Each command makes one purchase batch, up to 7,920 powders. Items remain in Inventory; the addon does not sell them or move them into storage.
Stop or Check Status
//acco cancel
//acco status
Cancellation stops further automation. A purchase already sent to the server may still complete.
Multiple Characters
With Windower’s Send addon installed and loaded:
Load Accolades on all connected characters:
//send @all lua load accolades
Request bulk purchases on all connected characters:
//send @all acco buyall prize powder
Every character must meet the location, distance, menu, and inventory requirements independently.
Stop all characters:
//send @all acco cancel
Updating
Replace both addon files, then reload:
//lua reload accolades
For all connected characters, using Send:
//send @all lua reload accolades
Reloading does not purchase anything.
Retries and Confirmation
- If the initial NPC contact receives no menu response, the addon allows up to three total contact attempts.
- Retry delays vary by character to reduce simultaneous requests.
- Retries stop if the character moves out of range, is no longer idle, or has another menu open.
- Later menu-stage timeouts stop the run rather than restarting it.
- Once a purchase is sent, it is never automatically resent.
- Success is reported when the expected increase in Inventory Prize Powder is observed.
- If purchase confirmation times out, check Inventory before retrying.
Important Notes
- Only Urbiolaine in Southern San d’Oria is supported.
- This is a separate addon from Sparks.
- Do not run other NPC-purchase automation simultaneously.
- Free Inventory space or room in an existing Prize Powder stack is required.
- Existing weekly exchange limits still apply.
- Single, bulk, and all-character purchasing have been reported working in-game; this does not guarantee every situation or client setup.
