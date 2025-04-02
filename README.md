# Connecting open science projects

A centralized platform with a searchable database and news feed to improve the discoverability of the open source ecosystem.

## Why?

The open source community is so big, with countless projects, it's a challenge to stay informed. Many projects remain unknown unless they are showcased at events or through grant proposals. This lack of visibility makes it difficult for community members to discover, connect, and collaborate effectively.

## What?

A centralized platform with a searchable database and news feed could greatly improve the discoverability of the open source ecosystem. Projects could share key information such as goals, contributor needs, and progress updates, allowing developers and users to easily find and connect with relevant initiatives. This centralized hub would foster greater collaboration and improve visibility across the community.

## Who?

Current contributors seeking projects or collaborators, new contributors exploring opportunities, and project leads looking for contributors and partners.

## Setup Instructions

### Prerequisites
- Python 3.11 or higher

### Installation

1. Clone this repository:
   ```
   git clone https://github.com/OpenScienceLabs/connecting-osp.git
   cd connecting-osp
   ```

2. Create and activate a virtual environment using uv:
   ```
   uv venv
   source .venv/bin/activate  # On Unix or macOS
   # OR
   .venv\Scripts\activate  # On Windows
   ```

3. Install the project dependencies:
   ```
   uv pip install -r pyproject.toml
   ```

### Running the Project

#### Using Quarto (Recommended)

With the virtual environment activated:

```
quarto preview
```

The website will be available at http://localhost:7719/ (or similar port).

#### Using Jupyter Lab (Alternative)

With the virtual environment activated:

```
jupyter lab
```

This will open a Jupyter Lab instance in your browser where you can explore and edit the project files. The Jupyter server typically runs at:
- http://localhost:8888/lab (a token will be provided in the terminal output)

## Project Structure

- `_quarto.yml` - Quarto configuration file
- `index.qmd` - Homepage
- `projects.qmd` - Projects listing
- `news.qmd` - News feed
- `about.qmd` - About page
- `styles.css` - Custom styles
- `images/` - Image assets
- `data/` - Data files

## Troubleshooting

### Common Issues

1. **"Module not found" errors**: Make sure your virtual environment is activated and dependencies are installed:
   ```
   source .venv/bin/activate  # On Unix or macOS
   # OR
   .venv\Scripts\activate  # On Windows
   uv pip install -e .
   ```

2. **Quarto not found**: The quarto-cli package should install Quarto automatically. If you have issues, try reinstalling the package:
   ```
   uv pip install --force-reinstall quarto-cli
   ```
