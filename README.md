## Overview

This document serves as the main landing page for the following documentation sites:
- [ExFlow Documentation](https://docs.exflow.cloud)
- [SignUp Software Documentation](https://docs.signupsoftware.com)

It provides a starting point for all product manuals and other documents such as "Terms of Agreements" and "Statement of Work". These pages can be accessed using the main menu defined in `/index.html`.

Additionally, this page manages the "shortcuts" to pages in the **Products** repository:
```
GitHub:
https://github.com/signupsoftware/Docs-Products

Website:
https://lively-flower-064383f03.4.azurestaticapps.net/
```

The site itself is not directly visible to users; instead, other sites fetch pages from it and display them within an `<iframe>`. The **Products** repository/site is a separate Docusaurus application.

## Creating a New Page Shortcut

To create a new page shortcut, follow these steps:

1. Create a folder at the root level with the desired shortcut name.
2. Inside that folder, create a file named `index.html` with the following content:
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="icon" type="image/x-icon" href="/resources/img/cropped-exflow-logo-icon-32x32.png">
        <link rel="stylesheet" href="../resources/CSS/proxy_page.css">
        <title>SignUp Software AB</title>    
    </head>
    <body class="background-image">
        <iframe src="https://lively-flower-064383f03.4.azurestaticapps.net/Agreements?lang=none" width="100%" height="100%" title="SignUp Software Agreements"></iframe>
<!--        <iframe src="https://thankful-ZZZwater-06a6c0b03.5.azurestaticapps.net/Agreements?lang=none" width="100%" height="100%" title="SignUp Software Agreements"></iframe> -->
    </body>
    </html>
    ```

3. Adjust the `<iframe>` `src` attribute to link to the target page in the **Products** site. For example:
    ```html
    <iframe src="https://lively-flower-064383f03.4.azurestaticapps.net/Agreements?lang=none" width="100%" height="100%" title="SignUp Software Agreements"></iframe>
    ```

### Adding Arguments

Arguments can be appended to the URL in the `<iframe>` `src` attribute. In the example above, `?lang=none` is added to the URL to hide the **Search** function in the top navbar.

