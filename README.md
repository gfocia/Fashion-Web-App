# Fashion Web App

This Django-based web application allows users to create profiles, post outfit ideas, browse and contribute to aesthetic-based fashion content, follow others, and view a personalized fashion feed. It supports a community of users sharing style inspiration and curated outfit suggestions through a clean, user-authenticated platform.

---

## Overview

The Fashion Web App enables users to:
- Create a personal profile with bio and image
- Browse and create fashion aesthetics
- Upload outfit ideas with style tags and images
- Receive curated outfit suggestions with shopping links
- Share public status messages with optional images
- Follow other users and view a news feed of their content
- Register, log in, and log out securely

---

## Core Components

### Models (`models.py`)
Defines the primary data structures:
- **Profile**: Linked to a Django user, includes bio, profile picture, and followers
- **Aesthetic**: Represents a named fashion style with a description and example image
- **OutfitIdea**: A user-submitted look associated with an aesthetic and optional image
- **OutfitSuggestion**: Curated outfit with a title, item list, image, and purchase links
- **StatusMessage**: Social-style post with a message and optional image
- **Friend**: Represents a bidirectional friendship between profiles

### Forms (`forms.py`)
Provides Django form classes for:
- Creating/updating profiles and aesthetics
- Submitting outfit ideas and outfit suggestions
- Posting status messages
- Creating users with extended profile data

### Views (`views.py`)
Implements all page logic using Django class-based views:
- List and detail views for profiles, aesthetics, ideas, and suggestions
- Authenticated create/update/delete views for posts and aesthetics
- Newsfeed-style homepage aggregating recent content
- User registration, login, and redirection logic

### URLs (`urls.py`)
Maps routes to views for:
- Profiles: creation, detail, update
- Aesthetics: browsing and creating
- Outfit ideas and suggestions: browsing and posting
- Posts: CRUD operations for status messages
- Authentication: login, logout, and registration
- Homepage and filtering by aesthetics

### Admin (`admin.py`)
Registers all models for the Django admin panel.

### App Configuration (`apps.py`)
Configures the app as `project` for Django to recognize.

---

## Features

- User registration and authentication
- Profile creation and image upload
- Follower and friendship systems
- Outfit posting tagged by aesthetics
- Structured fashion suggestions with shopping links
- Post creation, editing, and deletion
- Home feed with all fashion content in reverse chronological order
- Dynamic aesthetic filtering on ideas/suggestions pages

---

## Usage

### 1. Install dependencies:
```bash
pip install -r requirements.txt
pip install django pillow

### 1. Install dependencies:
```bash
pip install -r requirements.txt
pip install django pillow
