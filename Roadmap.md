# Roadmap for SpeleoGrammetry Project
## Goals
1. Centreline data from video
2. Vague passage reconstruction

## Operation
- Research
	- Opencv
	- OpenSSM
	- Colemap
	- Survex API
- Database management setup
- Pre-process video files -> frames
- Feature detect of frames
- Feature matching between frames
- 3x3 Matrix output from feature matches
- Smoothing/filtering of centre-line
- Displaying centreline in 3D
- Storing centreline in database
- Outputting centreline to file (survex .svx file)
- Producing survey [and extended elevation] vector files
- Attaching GPS Coords to points on the survey
- Knitting together multiple surveys/videos
	- 3D localisation/recognition?
	- 
- Loop closure recognition and error correction

## "Bread-Crumbing" Idea
- Emissive sources (small tripods with LEDs on) placed at regular, short invtervals along the passage
- These are "survey stations" and are super easy to localise with the camera
- Alternatively, have a few of these which you place at your start and end of your "legs" (sections of survey video footage)
- OR reflective surfaces / balls which are easily localised with a torch illuminating them
- _MICROPRISMATIC TAPE_

## Roadmap
1. Database schema/tables
	- SQlite
	- Async loop/queue for access
2. Video Input / Pre-Process
	- Receive lens info -> db
		- Calibration surface
	- Take video file, separate into frames
	- Reverse lens transform to each frame
	- Feature detect, write coords and the SIFT descriptor to database
3. Process
	- Feature matching from database to produce transformation matrices
	- Multiple scales of feature match
		- Neighbouring frames, two away, three away etc.
	- Process matrices on different scales to produce the centreline
	- Write centreline to database
4. Output
	- Output to .svx file
	- Use survex to produce topo, survey, etc.


## Milestones
### MILESTONE 1
	- Buy reflective tape
	- Video dark room with reflectors + torch
	- Produce model of room

