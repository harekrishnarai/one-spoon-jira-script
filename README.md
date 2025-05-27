# Jira Automation Scripts for Software Supply Chain Security

This repository contains a collection of Python scripts and Jupyter notebooks for automating common Jira tasks related to software supply chain security research and management.

## Contents

- [**label-adder.ipynb**](./label-adder.ipynb) - A script to add specific labels to Jira tickets in bulk.
- [**dev-status-checker.ipynb**](./dev-status-checker.ipynb) - A script to check if Jira tickets have associated development activity.

## Features

The scripts in this repository enable you to:

- Add labels to specific Jira tickets
- Check development status on tickets (PRs, commits, branches)
- Authenticate securely with Jira's API
- List accessible projects
- View and manipulate ticket metadata

## Requirements

- Python 3.6+
- Jupyter Notebook
- Required Python packages:
  - `requests`
  - `json`
  - `getpass`

## Setup

1. Clone this repository
2. Make sure you have Python and Jupyter Notebook installed
3. Install required dependencies:
   ```bash
   pip install requests jupyter
   ```
4. Create a Jira API token by following [Atlassian's documentation](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account/)

## Usage

### Label Adder Script

The `label-adder.ipynb` notebook allows you to add specific labels to Jira tickets:

1. Open the notebook in Jupyter or VS Code
2. Update the pre-filled variables:
   - `jira_url` - Your Jira instance URL
   - `email` - Your Jira account email
   - `ticket_keys_list` - List of Jira ticket keys to modify
3. Run the notebook cells
4. Enter your Jira API token when prompted
5. Confirm the operation when prompted

### Development Status Checker

The `dev-status-checker.ipynb` notebook checks whether Jira tickets have associated development activities (commits, PRs, branches):

1. Open the notebook in Jupyter or VS Code
2. Update the configuration variables:
   - `JIRA_DOMAIN` - Your Jira instance domain (e.g., "your-org.atlassian.net")
   - `JIRA_EMAIL` - Your Jira account email
3. Create a text file named `jira_links.txt` with one Jira ticket URL per line
4. Run the notebook cells
5. Enter your Jira API token when prompted
6. The script will output whether each ticket has associated development activities

## Security Notes

- API tokens are requested securely using the `getpass` module
- Tokens are not stored in the scripts
- Always keep your API tokens secure and never commit them to version control

## Future Improvements

- Add more reporting tools for supply chain security metrics
- Create functionality for bulk ticket updates
- Implement dashboard visualization for development activities
- Add support for filtering tickets by project or label

## Contributing

Feel free to contribute additional scripts or improvements to existing ones by submitting pull requests.

## License

[MIT License]
