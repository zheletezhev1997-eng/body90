# BECM BODY90

Public single-file BODY90 app for GitHub Pages.

- Live app: https://zheletezhev1997-eng.github.io/body90/
- Source repository: https://github.com/zheletezhev1997-eng/body90
- Supabase URL: https://avchydpvznglrknmaajv.supabase.co

## Telegram Mini App sign-in

The page includes the Telegram Web Apps SDK and a Telegram sign-in button. To enable it:

1. Apply supabase/telegram-auth.sql in the Supabase SQL Editor.
2. Deploy supabase/functions/body90-telegram-auth with JWT verification disabled (the function verifies Telegram initData itself).
3. Add the BotFather token to Supabase Edge Function secrets as TELEGRAM_BOT_TOKEN. Never put this token in the HTML or GitHub.
4. Configure the bot's Main Mini App in @BotFather with the live app URL.

Telegram identity links to an existing BODY90 account when the user is signed in; otherwise the function creates a dedicated Supabase Auth account. The function validates Telegram's signed initData server-side. It does not trust initDataUnsafe.

The app sends Telegram user ID and display name to the project's Supabase service for account creation/linking. The user must accept the app's data consent before cloud sync.

GitHub Pages serves this repository publicly. The browser bundle contains only the Supabase publishable key; the bot token and Supabase service-role key stay server-side.
