# Watson sentiment and emotion analysis

An IBM Developer Skills Network course project with a React interface and a Node.js/Express API for analysing text or a webpage URL through Watson Natural Language Understanding.

## Layout

- `sentimentAnalyzeClient/` — React application.
- `sentimentAnalyzeServer/` — Express API and served client build.

## API routes

The server listens on port 8080.

| Route | Input | Analysis |
| --- | --- | --- |
| `GET /url/emotion` | `url` query parameter | Keyword emotion |
| `GET /url/sentiment` | `url` query parameter | Keyword sentiment |
| `GET /text/emotion` | `text` query parameter | Keyword emotion |
| `GET /text/sentiment` | `text` query parameter | Keyword sentiment |

## Development setup

The pinned packages come from the original course environment. A Watson NLU service is required to exercise the analysis routes.

```sh
cd sentimentAnalyzeServer
npm install
```

Create a local `.env` in that directory containing your own `API_KEY` and `API_URL`.

In a separate terminal:

```sh
cd sentimentAnalyzeClient
npm install
npm start
```

The client's `npm run build` command builds React and copies the result into `sentimentAnalyzeServer/client`. Start the API with `npm start` from the server directory.

## Status

This repository is an earlier integration exercise. It demonstrates the React/Express/Watson request flow; it is not a finished production service. The server package's test command is still a placeholder, and live Watson requests have not been rerun for this documentation update.

## Attribution

Forked from [IBM Developer Skills Network](https://github.com/ibm-developer-skills-network/cazgi-IBM-Watson-NLU-Project). The original [licence](LICENSE) is retained.
