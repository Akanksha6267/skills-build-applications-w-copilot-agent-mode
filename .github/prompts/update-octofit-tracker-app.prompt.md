mode: agent
model: GPT-4.1

# Instructions to update Django project files in octofit-tracker/backend/octofit_tracker

## Update settings.py
- Ensure MongoDB (Djongo) is configured as the database backend.
- Enable and configure CORS to allow all origins, methods, and headers.

## Update/Create the following files to support users, teams, activities, leaderboards, and workouts:
- models.py: Define models for User, Team, Activity, Leaderboard, Workout.
- serializers.py: Create serializers for all models.
- views.py: Implement API views (ViewSets or APIViews) for all models.
- urls.py: Route / to the API root and expose endpoints for all models. Ensure api_root exists.
- tests.py: Add basic tests for all endpoints and models.
- admin.py: Register all models for Django admin.

## Requirements
- All endpoints must be available under /api/ (e.g., /api/users/, /api/teams/, etc.).
- The root URL (/) must route to the API root (api_root) with links to all endpoints.
- Use Django REST Framework best practices.
- Ensure all code is compatible with Djongo and MongoDB.
- Follow project conventions and keep code clean and well-documented.
