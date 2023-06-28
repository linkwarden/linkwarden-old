> **Warning** The following repo is no longer maintained. We **highly** recommend exploring the significantly enhanced rebuild, which can be found *[here](https://github.com/linkwarden/linkwarden)*.

<div align="center">
<h1>
Linkwarden
</h1>

[Demo (outdated version)](https://linkwarden.netlify.app/) | [Intro & Motivation](https://github.com/Daniel31x13/linkwarden#intro--motivation) | [Features](https://github.com/Daniel31x13/linkwarden#features) | [Setup](https://github.com/Daniel31x13/linkwarden#setup) | [Development](https://github.com/Daniel31x13/linkwarden#linkwarden-development)

</div>

## Intro & Motivation

**LinkWarden is a self-hosted, open-source bookmark + archive manager to collect, and save websites for offline use.**

The objective is to have a self-hosted place to keep useful links in one place, and since useful links can go away (see the inevitability of [Link Rot](https://www.howtogeek.com/786227/what-is-link-rot-and-how-does-it-threaten-the-web/)), LinkWarden also saves a copy of the link as screenshot and PDF.

## Features

* 📷 Auto-capture a screenshot and PDF from each website.

* 🔥 Sleek, minimalist design.

* 🌤 Dark/Light mode support.

* ↔️ Responsive design.

* 🔎 Search, filter and sorting functionality.

* 🚀 Lazy loading (for better performance).

* 🏷 Set multiple tags to each link.

* 🗂 Assign each link to a collection where we can further group links.

## Installation

### Using Docker Compose V2 (Recommended)

1. Make sure docker is installed.

2. Clone this repository.

3. Head to the main folder and run `docker compose up -d`.

The app will be deployed on port 3000.

### Configuration
To configure the app create a `.env` file (in the main folder), here are the available variables:
```
CLIENT_PORT=2500           # Default: 3000
API_PORT=5700              # Default: 5500
API_ADDRESS=192.168.1.14   # Default: localhost
```

> If you want to use this app across the network set `API_ADDRESS` as the computer (where LinkWarden is hosted) IP address.

### Manual Setup

1. Make sure your MongoDB database and collection is up and running.

2. Edit [URI, Database name and Collection name](api/config.js) accordingly.

3. [Optional] If you want to use this app across the network change [`API_HOST`](src/config.js) address with the computer IP and API port.

4. Head to the main folder using terminal and run: `(cd api && npm install) && npm install --legacy-peer-deps` for the dependencies.

5. Run `npm start` to start the application.

## LinkWarden Development

All contributions are welcomed! But first please take a look at [how to contribute](.github/CONTRIBUTING.md).

> **For questions/help, feature requests and bug reports please create an [issue](https://github.com/Daniel31x13/link-warden/issues) (please use the right lable).**
