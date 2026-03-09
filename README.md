# DJ-Organizer

## This is a GitHub Repository for the development of a DJ-Organization Tool for DIDA 425

## Project Idea 
* User Visits webpage (hosted on github pages)
* User Accesses their spotify account using O-Auth
* User selects playlist from their spotify library 
* Use Open Source Tool to convert spotify playlist to Raw Audio Files (found spotDL - CL software, may have issues if not a spotify premium user, also found https://lucida.to/ or other possibilities at https://fmhy.net/audio)
* Use Open Source Tool (potentially 'EchoNest') to extract audio features from audio files
* Using these audio features develop a collaborative filtering / recommendation system
* Use the collaborative filtering system to obtain similarity scores between songs and find the ordering which minimizes the total similarity differences between songs
* Output an ordered list of songs, and convert this list back into a spotify playlist and allow user to import it back into Spotify 

## Progress
* I have set up the spotify O-Auth to be able to access my own playlists and obtain a list of song ids from the playlist, we can possible use these song IDs to pass through music ripping sites
* Start of the frontend, have a basic html,java,css setup to start working forward 

## Next Up 
* The whole project hinges on being able to extract audio features from these out of data samples, so try and find a way to do this. 
* We will be looking into Essentia, an open source library of tools for audio and music analysis

## In Progress
* Working to more deeply understand the analysis structure
* Were able to see that the h5 files in the million subset has the following analysis parameters (can we replicate the same using another complementary analysis tool??? )

| Index | Feature Name                    |
|-------|----------------------------------|
| 1     | bars_confidence                 |
| 2     | bars_start                      |
| 3     | beats_confidence                |
| 4     | beats_start                     |
| 5     | sections_confidence             |
| 6     | sections_start                  |
| 7     | segments_confidence             |
| 8     | segments_loudness_max           |
| 9     | segments_loudness_max_time      |
| 10    | segments_loudness_start         |
| 11    | segments_pitches                |
| 12    | segments_start                  |
| 13    | segments_timbre                 |
| 14    | songs                           |
| 15    | tatums_confidence               |
| 16    | tatums_start                    |

