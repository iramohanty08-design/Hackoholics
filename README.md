# SkillBridge Assistant

A community-powered opportunity chatbot: **Skills → Service → Growth**.
It connects people's skills with NGO and community volunteering roles, and records their contribution history.

## Features
- **Skill profile**: type "I know Python and design posters in Chennai" and skills and city are extracted.
- **Post opportunities**: NGOs describe a role in chat and it is added to the board.
- **Smart matching**: roles are ranked by the share of required skills you cover, then by location, with an explanation.
- **Track the journey**: apply, mark completed, and build a contribution history.
- **Learning record**: the bot asks what you learned and saves it.
- **Success measures**: live counts of profiles, opportunities, matches, projects, learning notes and hours.

## Run it
No build step and no dependencies. Open `index.html` in a browser.

To host it free, enable **GitHub Pages** (Settings → Pages → deploy from the `main` branch, root folder).

## How it works
- `index.html` contains the page, styles and logic in one file.
- `SKILLS` maps each skill to keywords; `extractSkills()` and `extractCity()` read the user's message.
- `handle()` routes each message to an action (add skills, match, post a role, complete a project, show progress).
- Matching lives in `score()` and `matches()`.
- Opportunities are sample data in the `opps` array. State lives in memory, so a refresh resets it.

## Next steps
- Replace keyword matching with a Claude API call that returns JSON (skills, city, intent).
- Add a database (Supabase or Firebase) and login so profiles and roles persist.
- Add NGO approval of completed projects, and a shareable contribution record.

## License
MIT
