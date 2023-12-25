

# Gmail API Draft Creator

## Overview

This Python script leverages the Gmail API to create drafts for sending emails programmatically. It uses OAuth 2.0 for authentication and the Gmail API for interaction.

## Prerequisites

Before running the script, make sure you have the necessary dependencies installed. You can install them using:

```bash
pip  install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
```

Also, ensure that you have the required credentials. Follow the steps in the [Google API Python Quickstart guide](https://developers.google.com/gmail/api/quickstart) to set up your project and download the `credentials.json` file.

## Usage

1. Clone the repository:

```bash
git clone https://github.com/Gerodotry/Task.git
```

2. Install dependencies:

```bash
pip  install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
```

3. Run the script:

```bash
python create_draft.py
```

This will create a draft email with a specified subject, recipient email, and body text.

## Configuration

Make sure to configure the following variables in the script:

- `SCOPES`: List of OAuth 2.0 scopes required for Gmail API access.
- `FROM_EMAIL`: Your Gmail address used as the sender.
- `CREDENTIALS_FILE`: Path to the `credentials.json` file.
- `TOKEN_FILE`: Path to the token file storing OAuth 2.0 credentials.

## Example

```python
create_draft("Dan", "hello@gmail.com", "Discussing upcoming projects and deadlines.")
```

This example creates a draft email with the subject "Dan" sent to "hello@gmail.com" with the specified body text.

## Notes
Exception Handling:

- The script uses a try-except block to catch HttpError exceptions that might occur during Gmail API interactions. If an error occurs, it prints an error message, and the variable draft is set to None.
- The script checks for existing OAuth 2.0 credentials and refreshes them if necessary.
- Ensure that the Gmail API is enabled for your Google Cloud project.

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to expand and modify this README to better suit your project's documentation needs.
