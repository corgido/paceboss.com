# PaceBoss

Local-first race analysis for Assetto Corsa Competizione.

🔗 **Live app:** [paceboss.com](https://paceboss.com)


## What it does

PaceBoss is a local-first race analytics platform for Assetto Corsa Competizione
(ACC) that enables Console sim racers to track their own performance. Users drop a
race export file into the browser and get a full driver analysis dashboard — no
accounts, no uploads, no server persistence. All data stays in IndexedDB on the
user's device.

The app ingests two formats: SimResults.net CSV reports (structured text with
embedded tables, not simple CSV) and ACC native server JSON (UTF-16LE encoded). It
normalizes both into a canonical relational model and derives analytical metrics
per driver per session.

## Why

I wanted to understand and aggregrate race data and present it within a design system.

## Stack

React 18 + TypeScript 5.8 + Vite

## Career View
As drivers accumulate sessions, the "Me" page becomes a record of bests and trends
![PaceBoss Career](/images/paceboss_sample_1.png)

## Race Details
Part of going faster is about the gap between Theoretical Best and Personal Bests - if this delta is large, then it's probably a consistency problem. If there gap is difficult to distinguish then it's probably a ceiling problem and requires technique, training, or may just be the natural limit.

PaceBoss inverts the typical - if the line is flat and close to the TB/PB, then that's a good race. But the laptime itself doesn't tell the complete story, a lap is the combination of its sectors each with its unique challenges. 

![PaceBoss Race Graph](/images/paceboss_sample_3.png)



This **sector view**, enables at a glance digestion of the sector performance to help identify where the pace could be gained.

![PaceBoss Sector Graph](/images/paceboss_sample_2.png)
