<details>
<summary>Details of Nxt Watch webpage</summary>

Implemented Nxt Watch application which is a clone for YouTube where users can log in and can see a list of videos like Trending, Gaming, Saved videos, and also can search videos and view specific video details, and users can toggle the theme (Light/Dark).

Implemented Different pages like Login, Home, Trending, Gaming, Saved videos using React components, props, state, lists, event handlers, form inputs.
Authenticating by taking username, password and doing login post HTTP API Call.
Persisted user login state by keeping jwt token in local storage, Sending it in headers of further API calls to authorize the user.
Implemented different routes for Login, Home, Trending, Gaming, Saved videos, Video item details pages by using React Router components Route, Switch, Link.
Redirecting to the login page if the user tries to open Home, Trending, Gaming, Saved videos, Video item details routes which need authentication by implementing protected Route.
Technologies used: React JS, JS, CSS, Bootstrap, Routing, REST API Calls, Local Storage, JWT Token, Authorization, Authentication.
</details>

### Set Up Instructions

<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

<summary>API Requests & Responses</summary>
<br/>

**loginApiUrl**

#### API: `https://apis.ccbp.in/login`

#### Method: `POST`

#### Description:

Returns a response containing the jwt_token

#### Success Response

```json
{
  "jwt_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InJhaHVsIiwicm9sZSI6IlBSSU1FX1VTRVIiLCJpYXQiOjE2MTk2Mjg2MTN9. nZDlFsnSWArLKKeF0QbmdVfLgzUbx1BGJsqa2kc_21Y"
}
```

#### Failure Response

```json
{
  "status_code": 404,
  "error_msg": "Username is not found"
}
```

**homeVideosApiUrl**

#### API: `https://apis.ccbp.in/videos/all?search=`

#### Method: `GET`

#### Description:

Returns a response containing the list of all videos

#### Response

```json
{
  "total": 60,
  "videos": [
    {
      "id": "30b642bd-7591-49f4-ac30-5c538f975b15",
      "title": "Sehwag shares his batting experience in iB Cricket | iB Cricket Super Over League",
      "thumbnail_url": "https://assets.ccbp.in/frontend/react-js/nxt-watch/ibc-sol-1-img.png",
      "channel": {
        "name": "iB Cricket",
        "profile_image_url": "https://assets.ccbp.in/frontend/react-js/nxt-watch/ib-cricket-img.png"
      },
      "view_count": "1.4K",
      "published_at": "Apr 19, 2019"
    },
    ...
  ],
}
```

**trendingVideosApiUrl**

#### API: `https://apis.ccbp.in/videos/trending`

#### Method: `GET`

#### Description:

Returns a response containing the list of trending videos

#### Response

```json
{
  "total": 30,
  "videos": [
    {
      "id": "ad9822d2-5763-41d9-adaf-baf9da3fd490",
      "title": "iB Hubs Announcement Event",
      "thumbnail_url": "https://assets.ccbp.in/frontend/react-js/nxt-watch/ibhubs-img.png",
      "channel": {
        "name": "iB Hubs",
        "profile_image_url": "https://assets.ccbp.in/frontend/react-js/nxt-watch/ib-hubs-img.png"
      },
      "view_count": "26K",
      "published_at": "Nov 29, 2016"
    },
    ...
  ]
}
```

**gamingVideosApiUrl**

#### API: `https://apis.ccbp.in/videos/gaming`

#### Method: `GET`

#### Description:

Returns a response containing the list of gaming videos

#### Response

```json
{
  "total": 30,
  "videos": [
    {
      "id": "b214dc8a-b126-4d15-8523-d37404318347",
      "title": "Drop Stack Ball",
      "thumbnail_url": "https://assets.ccbp.in/frontend/react-js/nxt-watch/drop-stack-ball-img.png",
      "view_count": "44K"
    },
    ...
  ]
}
```

**videoItemDetailsApiUrl**

#### API: `https://apis.ccbp.in/videos/:id`

#### Example: `https://apis.ccbp.in/videos/802fcd20-1490-43c5-9e66-ce6dfefb40d1`

#### Method: `GET`

#### Description:

Returns a response containing the list of gaming videos

#### Response

```json
{
  "video_details": {
    "id": "ad9822d2-5763-41d9-adaf-baf9da3fd490",
    "title": "iB Hubs Announcement Event",
    "video_url": "https://www.youtube.com/watch?v=pT2ojWWjum8",
    "thumbnail_url": "https://assets.ccbp.in/frontend/react-js/nxt-watch/ibhubs-img.png",
    "channel": {
      "name": "iB Hubs",
      "profile_image_url": "https://assets.ccbp.in/frontend/react-js/nxt-watch/ib-hubs-img.png",
      "subscriber_count": "1M"
    },
    "view_count": "26K",
    "published_at": "Nov 29, 2016",
    "description": "iB Hubs grandly celebrated its Announcement Event in November 13, 2016, in the presence of many eminent personalities from the Government, Industry, and Academia with Shri Amitabh Kant, CEO, NITI Aayog as the Chief Guest."
  }
}
```

</details>

- User credentials

  ```text
   username: rahul
   password: rahul@2021

  ```

