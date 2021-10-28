## group spotify analysis
analysis of spotify data from multiple people. 

## submitting data
to get your spotify data, request it from the spotify website. ([link](https://www.spotify.com/us/account/privacy/)) it says it should arrive within 30 days but it's usually around 3. when it's done you'll get a zip file with json files in it. download this and:

1. unzip the zip folder
2. in the unzipped folder, delete all the files except for the stream history files, which are of the form `StreamingHistoryX.json` where `X` is a number from `0` to `n` if you have `n+1` files. note: the reason we ask you to delete everything except the stream history is that some of the data is personal (e.g., payment information etc.)
3. re-zip this folder and name the zip file `firstname_lastname.zip`
4. fork the repo and put your zip file in the `zips` folder
5. make a pull request from your branch with the comment "data submission"

pull requests will be reviewed promptly and then the data will be added to our dataset for use in analysis.

## goals (ranked roughly by difficulty)

- [] make histograms of listening data by time of year, day of week, and hour of day
- [] in what areas do submitters overlap in their listening habits? (tracks, artists, ...)
- [] visualize the density of track listens by release date. are people listening to songs released in a specific timeframe?
- [] make video of top artists over time (see [here](https://www.youtube.com/watch?v=4f6-MDhygWc) for reference video)
- [] make heatmap of locations of artists by country of origin
- [] use spotify api to get genres and other characteristics of tracks. draw conclusions based on the relative amounts of each genre listened to throughout the year. are there seasonal patterns? what about other characteristics, such as danceability, energy, acousticness, etc.? what about time of day or week rather than time of year?
- [] make a generalized function to create a radar chart comparing two submitters (or one submitter and the current top 100 songs) on various metrics (e.g., danceability, energy, etc.) using overlapping colors
- [] click-off times: are there songs that are frequently skipped? how long does it take for someone to determine that they want to skip a song?
- [] with a given day's worth of track-listening data, can we predict the next track that a user will listen to?
- [] can we isolate "novelty tracks"? define a novelty track as one which does not fit in with the tracks listened to around it, e.g. [half of a taylor swift album] + [politikz: "real hip hop"] + [the other half of the taylor swift album] => [politikz: "real hip hop"] is a "novelty track". we expect these tracks to include such titles as tay-k: "the race", and bhad bhabie: "gucci flip flops". can we get a list of these such tracks?
- [] sentiment analysis (lyrics of songs from another api): can we determine the efficacy of spotify's api regarding the genre of a track by comparing it to a sentiment analysis of its lyrics? can we go the other way -- that is, could we train a sentiment analysis model based on lyrics + the spotify api's genre assignment for that track?
- [] can we check the efficacy of spotify's playlist shuffling? we'd determine whether, in a given span of tracks, a user is listening to a playlist. then, we'd determine whether the playlist is in order given the original ordering, and then convert the song orders to indices in future playlist-listening-sessions. with these groups of indices, can we reverse-engineer the spotify playlist-shuffling algorithm?
