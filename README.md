# Hunter Journal Server

This repository is a [json-server](https://github.com/typicode/json-server) API created to feed data into the Hunter Journal React application.

#### [Client Repo here](www.your-github-url-here.com)

## Setup

Install dependencies:

```bash
npm install
```

Start the server:

```bash
npm start
```

For development with automatic restarts:

```bash
npm run dev
```

The server runs on `http://localhost:5005` by default. To use a different port, add a `.env` file with:

```bash
PORT=5005
```

# Server Structure

## Collections

### locations

```javascript
{
  id,
  location,
  mapImage,
  images,
  enemyIds,
  tramAccess,
  description,
}
```

### enemies

```javascript
{
  id,
  name,
  images,
  briefDescription,
  behaviour,
  health,
  geo,
  locationIds,
}
```

## Used API Endpoints in the App

| HTTP Method | URL                       | Request Body                                                                 | Description                         |
| ----------- | ------------------------- | ---------------------------------------------------------------------------- | ----------------------------------- |
| GET         | `/locations`              |                                                                              | Sends all locations                 |
| POST        | `/locations`              | `{location, mapImage, images, enemyIds, tramAccess, description}`             | Creates a new location              |
| GET         | `/locations/:locationId`  |                                                                              | Sends details for one location      |
| PUT         | `/locations/:locationId`  | `{location, mapImage, images, enemyIds, tramAccess, description}`             | Replaces a location object          |
| PATCH       | `/locations/:locationId`  | Partial location object                                                       | Edits part of a location object     |
| DELETE      | `/locations/:locationId`  |                                                                              | Deletes a location object           |
| GET         | `/enemies`                |                                                                              | Sends all enemies                   |
| POST        | `/enemies`                | `{name, images, briefDescription, behaviour, health, geo, locationIds}`        | Creates a new enemy                 |
| GET         | `/enemies/:enemyId`       |                                                                              | Sends details for one enemy         |
| PUT         | `/enemies/:enemyId`       | `{name, images, briefDescription, behaviour, health, geo, locationIds}`        | Replaces an enemy object            |
| PATCH       | `/enemies/:enemyId`       | Partial enemy object                                                          | Edits part of an enemy object       |
| DELETE      | `/enemies/:enemyId`       |                                                                              | Deletes an enemy object             |

## Useful Query Examples

| URL                                  | Description                                   |
| ------------------------------------ | --------------------------------------------- |
| `/enemies?name=Crawlid`              | Finds enemies with the name `Crawlid`         |
| `/enemies?locationIds_like=hk_area_009` | Finds enemies connected to a location id   |
| `/locations?enemyIds_like=enemy_0001` | Finds locations connected to an enemy id     |
| `/locations?tramAccess=true`         | Finds locations with tram access              |

## Links

### Collaborators

[Developer 1 name](www.github-url.com)

[Developer 2 name](www.github-url.com)

### Project

[Repository Link Client](www.your-github-url-here.com)

[Repository Link Server](https://github.com/Yemi7/hunter-journal-server)

[Deploy Link](www.your-deploy-url-here.com)

### Trello

[Link to your trello board](www.your-trello-url-here.com)

### Slides

[Slides Link](www.your-slides-url-here.com)
