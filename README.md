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
- Install `uv`

### Installation

1. Clone this repository:
   ```
   git clone https://github.com/OpenScienceLabs/connecting-osp.git
   cd connecting-osp
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv venv
   source venv/Scripts/activate  # On Windows with Git Bash
   # OR
   venv\Scripts\activate  # On Windows with CMD
   # OR
   .\venv\Scripts\activate  # On Windows with PowerShell
   ```

3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```
   
   Note: If you encounter any issues with PyYAML during the Quarto rendering process, make sure it's installed:
   ```
   pip install pyyaml
   ```

### Running the Project

#### Using Quarto (Recommended)

With the virtual environment activated:

```
quarto preview
```

If Quarto is not in your PATH, use the full path to the executable:

```
"C:/Program Files/Quarto/bin/quarto.exe" preview  # For default installation
```

Important notes:
- Make sure your virtual environment is activated when running Quarto
- Quarto will use the Python from your activated environment
- The website will be available at http://localhost:7719/ (or similar port)
- If you see an error about missing 'yaml' module, run `pip install pyyaml` in your activated environment

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

1. **"Module not found" errors**: Make sure your virtual environment is activated and all dependencies are installed.
   ```
   source venv/Scripts/activate  # On Git Bash
   pip install -r requirements.txt
   ```

2. **Quarto not found**: If running `quarto` commands results in "command not found", use the full path to the Quarto executable.

3. **Missing Python modules during Quarto rendering**: Quarto needs to use the Python from your virtual environment. Make sure to run Quarto commands with your virtual environment activated.

