# FULLSTACK AI CHATBOT

## Description

This is a general-purpose chatbot application, similar to Open AI's famous ChatGPT, but instead uses Google's Gemini 1.0 Pro model. It also has the advantage of being able to be configured to provide personalized responses and it has the characteristic of being embedded in the page, so that it can be folded and unfolded with a button, like typical consultation chats. Note that in this repository there are the two folders of the fullstack project for demonstration purposes: but in truth, they are two individual projects deployed separately.

### Stack

- HTML
- CSS
- JavaScript
- React (Vite JS)
- Express
- Vercel

## Setup

First of all you must clone the repository:

```sh
git clone https://github.com/jezbravo/brave-bot.git
cd brave-bot
```

Then install the dependencies:

```node
npm install
```

### Environment Variables

In order for the program to work correctly, it is necessary to configure the following environment variable in an **.env** file at the root of the server folder:

```javascript
GENAI_API_KEY=
```

This key is provided by the Google Gemini API service.

## Additional settings

### AI Assistant Name and Custom Responses

In the **index.js** file from server\api, you can configure the model by editing, for example, the history:

```javascript
history: [
      {
        role: "user",
        parts: [
          {
            text: "You are an AI virtual assistant and your name is Luna, also known as BraveBot.
          },
        ],
      },
],
```

## Demo

The interface tries to be as intuitive and friendly as possible. The virtual assistant has 3 possible states according to how the conversation unfolds, represented by some nice icons: "satisfactory response / greeting"; "thinking" and "error."

You can test a version deployed to production at the following link: https://react-chatbot-client.vercel.app
