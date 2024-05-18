# Notion Page to Markdown Exporter

This script checks if secrets and variables are correctly obtained in GitHub Actions, retrieves the content of a page from the Notion API, and saves it in Markdown format.

## Environment Variables

- `NOTION_API_KEY`: Authentication key for the Notion API.
- `PAGE_ID`: ID of the Notion page.
- `FILE_NAME`: Name of the file to save the content.

## Author

Takashi SASAKI  
Homepage: [https://x.com/TakashiSasaki](https://x.com/TakashiSasaki)

## Usage

1. Ensure you have a `.env` file with the necessary environment variables:

    ```plaintext
    NOTION_API_KEY=your_notion_api_key
    PAGE_ID=your_page_id
    FILE_NAME=your_output_file.md
    ```

2. Install the required Python packages:

    ```sh
    pip install requests python-dotenv
    ```

3. Run the script:

    ```sh
    python export-notion-page.py
    ```

## Script Details

The script includes the following main functions:

### `get_env_variable(var_name)`

Retrieves the value of an environment variable. Raises an exception if the variable is not found.

### `get_page_content(page_id)`

Fetches the content of the specified Notion page using the Notion API.

### `notion_to_markdown(content)`

Converts the content of a Notion page to Markdown format.

## Debug Output

The script prints debug information, such as the values of environment variables and the status of API requests, to the console.

## Error Handling

The script handles errors such as missing environment variables and issues with API requests by printing error messages and exiting gracefully.

## Example Output

An example of the Markdown content saved by the script:

```markdown
# Example Heading

This is an example paragraph.

## Example Subheading

- Example bullet point
- Another bullet point

1. Example numbered list item
2. Another numbered list item

> Example quote
