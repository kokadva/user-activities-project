# User Activity Management Application

## Objective
Build a web application using Django that allows the management of users and their associated activities. The application must enable specific CRUD operations on users and activities, where the calories burned for each activity are computed via the [API-Ninjas Calories Burned API](https://api-ninjas.com/api/caloriesburned).

## Models

### User
- `name`: First name of the user.
- `surname`: Last name of the user.
- `activities`: Relationship to the Activity model.

### Activity
- `activity_name`: Name of the activity.
- `duration`: Duration of the activity in minutes.
- `calories_burned`: Calorie count burned during the activity (calculated using the API-Ninjas Calories Burned API).
- `user`: Foreign Key relation to the User model (Each activity is associated with a user).

## Functionality

### User Management
- Create new users (with name and surname).
- Read user information (name and surname) along with their associated activities.
- Delete users.

### Activity Management
- Add activities for users (Calories burned should be calculated using the API-Ninjas Calories Burned API and saved in the database).
- Remove activities.

### API Endpoints
- Users:
  - Create, Read (including activities), Delete
- Activities:
  - Create, Delete (for specific users)
