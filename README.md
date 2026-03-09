# educera-your-full-time-batchie
EDUCERA: Your Full Time Batchie

EDUCERA is a web-based student productivity platform built on the Internet Computer (ICP) blockchain. It helps school and college students in India manage daily attendance, self-assigned tasks, and subject notes with AI-enriched resources — all in one place, accessible from any device with no installation required.

--------------------

## What It Does

EDUCERA gives students a personal study companion with four core modules:

Attendance Tracking — Log classes attended and topics covered per subject. View history in a list view, edit any record, and the app prevents duplicate entries for the same subject on the same day.

Task Management — Self-assign daily or weekly tasks with due dates and priority levels. Mark tasks complete with a single tap. Tasks are not restricted to subjects, so you can add anything like "Sleep 8 hours" or "Revise Chemistry Chapter 3". Tracks completion streaks.

Subjects and Notes — Add subjects, upload notes (text/PDF/image), and access AI-enriched resources per subject. School students get a dedicated PYQ (Previous Year Questions) section. College students get Important Questions categorized as Easy, Medium, or Hard. A Resources tab provides downloadable links to NCERT books, CBSE sample papers, university papers, and NPTEL lectures.

Dashboard — A summary view with count-up animated stat cards showing today's attendance, pending tasks, total notes, and current streak.

--------------------

## Who It Is For

School students in Classes 8 to 12 (CBSE and state board curricula).

College students in any degree program including BTech, BBA, BA, BSc, BCom, BCA, MBA, MBBS, BDS, BAMS, Nursing, LLB, Architecture, and Diploma programs.

--------------------

## Tech Stack

Frontend: React, TypeScript, Tailwind CSS, Framer Motion

Backend: Motoko (Internet Computer native language)

Hosting: Deployed on the Internet Computer (ICP) blockchain — no traditional server or cloud provider

Authentication: Custom username and password system with localStorage-based session persistence

--------------------

## Authentication

Students register with a username and password of their choice. Sessions persist across visits using localStorage.

Admin credentials are required for the admin panel (see Admin Panel section below).

--------------------


## Presentation Page

A built-in presentation walkthrough is available at /presentation. It includes 11 animated sections covering the problem statement, solution, all features, tech stack, ICP vs traditional hosting comparison, future scope, and team credits.

This page is designed to be opened fullscreen during college presentations with floating navigation dots for easy section jumping.

--------------------

## Project Structure

src/backend/main.mo — Core Motoko backend with all data models and API functions

src/backend/authorization/ — Role-based access control mixin

src/backend/blob-storage/ — File and blob storage mixin

src/frontend/src/pages/ — One file per page: Landing, Onboarding, Dashboard, Attendance, Tasks, Subjects, Admin, Presentation

src/frontend/src/components/ — Shared UI components

src/frontend/src/hooks/ — Custom React hooks

--------------------

## Data Models

UserProfile — name, level (school/college), education class, subjects list

Subject — id, name, level, createdAt

AttendanceRecord — id, subjectId, subjectName, date, topicCovered, attended, createdAt

Task — id, title, subjectName, dueDate, priority, completed, createdAt

Note — id, subjectId, subjectName, title, content, AI fields (summary, key topics, short notes, PYQs), uploadedAt

--------------------

## Built By

Suraj Kumar — surajkumarg1209@gmail.com

Ayush Singh — ayush342006@gmail.com

--------------------

## Future Scope

Real AI API integration (Groq / OpenAI) for live note enrichment

Teacher and parent dashboard roles

Push reminders for tasks and attendance

Collaborative notes between students

Multi-language support

Study timer and flashcard revision mode
