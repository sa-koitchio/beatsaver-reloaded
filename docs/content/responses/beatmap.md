# Beatmap Response

The Beatmap response contains data of an individual map:

| JSON Key     | Datatype     | Description    |
| :------------- | :----------: | -----------: |
|  name | String   | The name of the map shown on the website   |
| key  | String | The key is used to link to the map and can be used to identify a map  |
| \_id | String | --- |
| deletedAt | String | The timestamp the map got deleted at |
|description | String| The map's description on the website|
|uploaded| String| Timestamp of the uploaddate |
|hash | String | Used for leaderboards |
|directDownload| String | Direct link to the CDN server|
|downloadURL| String | Link using the api baselink to download|
|coverURL| String | Link to the map cover on the CDN server|
|metadata | JSON | JSON Object containing metadata on the beatmap|
|stats| JSON | JSON Object containing stats like plays, downloads, i.e. |
|uploader | JSON | JSON Object containing information on the user who uploaded the map|

## More info on the "metadata" JSON Object:

| JSON Key     | Datatype     | Description    |
| :------------- | :----------: | -----------: |
|duration | integer | The song length |
|automapper | String | Returns the name of the automapper (null if not automapped)|
|levelAuthorName| String | Level author's name|
|songAuthorName| String | The song artist's name|
|songName | String | Song name|
|songSubName | String | The little info shown below the song name in-game|
|bpm| int | The BPM of the song|
|characteristics| Array / List| Only has one element ("0") most of the time|
|difficulties| JSON | Stores info on the map's difficulty levels

## --> More info on the "characteristics" JSON Object / Array nested in "characteristics"
To get the JSON Object, use an integer value on the "characteristics" array. This will return a JSON Obj. for the corresponding gamemode

| JSON Key     | Datatype     | Description    |
| :------------- | :----------: | -----------: |
|name | String | Gamemode label (Standard, 90 deg.  etc.) |
|difficulties | JSON | JSON containing info on the different difficulties|

## --> More info on the "difficulties" JSON Object nested in "metadata"

| JSON Key     | Datatype     | Description    |
| :------------- | :----------: | -----------: |
|easy| boolean | True = map contains "easy" difficulty|
|normal| boolean | True = map contains "normal" difficulty|
|hard| boolean | True = map contains "hard" difficulty|
|expert| boolean | True = map contains "expert" difficulty|
|expertPlus| boolean | True = map contains "expertPlus" difficulty|


## --> More info on the "stats" JSON Object nested in [main json]

| JSON Key     | Datatype     | Description    |
| :------------- | :----------: | -----------: |
|downloads| integer | Number of downloads|
|plays| integer | Number of registered plays|
|downVotes| integer| Number of downvotes|
|upVotes| integer | Number of upvotes|
|heat| float | "Heat" value (used for determining popularity)|
|rating| float| The upvote/downvote ratio |

## --> More info on the "uploader" JSON Object nested in [main json]

| JSON Key     | Datatype     | Description    |
| :------------- | :----------: | -----------: |
|\_id| String | The user's ID|
|username| String | The user's nickname|

[Currently unfinished]
