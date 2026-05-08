# StudySync JJAY
A study group matcher for John Jay College students — built for the way you actually study.

## What it does
StudySync JJ helps John Jay students find compatible study partners based on three things most matcher apps ignore: not just what courses you're taking, but when you're free and how you like to study. No more getting paired with someone who wants to chat when you need to grind.

## Features
Study Vibe Matching — Students pick a study personality when they sign up: Silent Grinder, Explainer, Casual Collaborator, or Crunch Mode. The matching algorithm weighs vibe compatibility alongside course overlap so you actually mesh with your study partner.
Smart Matching Algorithm — Compatibility scores are calculated from three signals: shared courses (45%), vibe compatibility (35%), and overlapping availability (20%). Every student in browse is ranked by how well they match you specifically.
Availability Heatmap — A simple grid showing morning, afternoon, and evening slots across the week. Toggle your free times and the matcher factors them in automatically.
XP & Leaderboard — Earn points for actions inside the app: signing up, adding courses, completing study sessions, daily check-ins, and forming groups. The leaderboard ranks students by total XP — no self-reporting, no cheating.
Daily Streaks — Study (or check in) every day to build your streak. Hit 7 days and earn a fire badge. Stored locally so it persists across sessions.
Session Timer — Hit "Start Session" when you sit down to study with someone. The live stopwatch tracks your time. End the session and XP is automatically awarded.
Direct Messages — Message any student directly from their profile. Good for coordinating before a session or just breaking the ice.
Course Tags — Filter students by course code (CSCI 272, MTH 241, etc.) to find people in the same class fast.

## OOP Structure
The app is organized around four core classes:
Student — holds name, major, year, bio, courses, vibe, availability, LinkedIn, XP, and streak data.
VibeProfile — an enum-style object defining the four study styles and a compatibility scoring matrix between each combination.
MatchEngine — takes two Student objects and returns a compatibility score using weighted signals across courses, vibe, and availability. Also handles sorting the browse feed.
StudySession — manages the timer state, calculates duration on end, awards XP to the current user, and logs session history.

How to run it
This is a fully client-side app — no server, no install, no dependencies.

Download or clone this repo
Open studysync.html in any modern browser (Chrome recommended)
That's it

Tech stack
Pure HTML, CSS, and vanilla JavaScript. No frameworks, no build tools, no backend. All state lives in memory during the session; streaks and XP persist via localStorage.

##Future improvements
Firebase backend for persistent data and real-time DMs
Email login tied to a john.jay.cuny.edu address for verified student profiles
Push notifications for streak reminders
Group sessions with more than two students
Integration with the official John Jay course catalog

<sup>Team CSS
Built for CS DEPT. X CSS Hackathon at John Jay College of Criminal Justice.</sup>
