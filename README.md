# Seo Skills

A collection of reusable SEO skills for AI coding and writing assistants. Each skill is a self-contained folder with a `SKILL.md` that tells an assistant how to carry out one SEO task well, such as auditing a page, researching keywords, or writing meta tags.

> **Status:** early stage. The repository currently contains the license and this README. Skills are being added.

## Table of Contents

- [What are skills?](#what-are-skills)
- [Repository structure](#repository-structure)
- [Skills](#skills)
- [Installation](#installation)
- [Usage](#usage)
- [Creating a new skill](#creating-a-new-skill)
- [Contributing](#contributing)
- [License](#license)

## What are skills?

A skill is a folder of instructions (and optional scripts or reference files) that an AI assistant loads when a task matches the skill's description. Instead of re-explaining your SEO process in every prompt, you install the skill once and the assistant follows the same checklist every time.

## Repository structure

```
Seo-Skills/
├── skills/
│   └── <skill-name>/
│       ├── SKILL.md          # Required: name, description, instructions
│       ├── references/       # Optional: checklists, templates, glossaries
│       └── scripts/          # Optional: helper scripts
├── .gitattributes
├── LICENSE
└── README.md
```

## Skills

Add one row per skill as the collection grows.

| Skill | Purpose |
| ----- | ------- |
| _coming soon_ | _e.g. technical SEO audit_ |
| _coming soon_ | _e.g. keyword research and clustering_ |
| _coming soon_ | _e.g. on-page optimization and meta tags_ |
| _coming soon_ | _e.g. content briefs_ |

## Installation

Clone the repository:

```bash
git clone https://github.com/WHOISABHISHEKADHIKARI/Seo-Skills.git
cd Seo-Skills
```

Then copy the skill folders you want into your assistant's skills directory. The location depends on the tool you use (for example, a `.claude/skills/` folder in your project or home directory).

```bash
cp -r skills/<skill-name> <your-skills-directory>/
```

## Usage

Once a skill is installed, ask your assistant for the task in plain language. The assistant matches your request to the skill's `description` and follows its instructions.

Example prompts:

- "Audit this page for on-page SEO issues."
- "Group these keywords by search intent."
- "Write a title tag and meta description for this article."

## Creating a new skill

1. Create a folder under `skills/` with a short, lowercase, hyphenated name.
2. Add a `SKILL.md` with frontmatter:

   ```markdown
   ---
   name: your-skill-name
   description: One or two sentences on what the skill does and when to use it.
   ---

   # Your Skill Name

   Step-by-step instructions, checklists, and output format.
   ```

3. Keep the description specific. It decides when the assistant uses the skill.
4. Put long reference material in `references/` and keep `SKILL.md` focused.
5. Add the skill to the table in this README.

## Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a branch: `git checkout -b feat/your-skill-name`.
3. Add or improve a skill and update the table above.
4. Open a pull request describing what the skill does and how you tested it.

Please open an issue first for large changes.

## License

Released under the [MIT License](LICENSE).

## Author

Maintained by [Abhishek Adhikari](https://github.com/WHOISABHISHEKADHIKARI).
