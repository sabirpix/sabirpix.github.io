# Private Messaging App

Backend-first multi-user messaging application.

## Security model

Firebase Authentication answers **who is the user?**

Node.js answers **is the user allowed?**

Firestore stores **application metadata and relationships**.

Telegram stores **large media binaries**.

Never trust user-supplied `userId` fields as identity. The only identity source for protected routes is the verified Firebase ID token and `req.user.uid`.

## Important credential note

Do not commit a Telegram bot token or Firebase service-account private key. If a real Telegram token was exposed while setting up this demo, revoke it with BotFather and create a replacement token.
