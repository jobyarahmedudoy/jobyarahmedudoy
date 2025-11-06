import json


TEMPLATE = """
# 👋 Hi, I'm {name}
> {tagline}


## 🌟 About Me
- **Role:** {role}
- **Education:** {education}
- **Location:** {location}
- **Email:** {email}
- **LinkedIn:** {linkedin}
- **Portfolio:** {portfolio}


## 🧠 Skills
{skills}


## 🚀 Projects
{projects}
"""


def generate_readme(profile, out='README.md'):
content = TEMPLATE.format(**profile)
with open(out, 'w', encoding='utf-8') as f:
f.write(content)
print(f'Readme saved to {out}')
