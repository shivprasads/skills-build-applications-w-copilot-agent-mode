---
applyTo: "**"
description: |
  OctoFit Tracker project conventions and agent rules for all files and commands.
---

# OctoFit Tracker Agent Instructions

## Hard Rules

- Never change directories when running commands in agent mode. Always use absolute or project-relative paths.
- Only use the following ports for forwarding or public access:
  - 8000 (backend)
  - 3000 (frontend)
  - 27017 (MongoDB, private only)
- Do not propose or use any other ports for forwarding or public access.
- Use Django ORM for all database structure and data creation. Never use direct MongoDB scripts for schema/data setup.
- For checking MongoDB status, always use: `ps aux | grep mongod`
- Use the provided Python virtual environment at `octofit-tracker/backend/venv` for all backend Python operations.
- Install only the packages listed in `octofit-tracker/backend/requirements.txt` for the backend.

## Project Structure

- Backend: `octofit-tracker/backend/`
- Frontend: `octofit-tracker/frontend/`
- Python venv: `octofit-tracker/backend/venv/`

## Preferences

- Be concise in output, avoid unnecessary verbosity.
- Prioritize actionable results over process explanations.
- Use the same tokens/terms as user instructions wherever possible.

## Example Prompts

- "Set up the backend environment for OctoFit Tracker."
- "Check if MongoDB is running."
- "Install backend dependencies."
- "Never change directories in agent mode."

## Related Customizations to Consider

- Add file-specific instructions for Django or React code style.
- Create prompts for common setup or troubleshooting tasks.
- Define agent hooks for environment validation.
