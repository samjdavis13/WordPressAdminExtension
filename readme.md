# WordPressAdmin Algorythm

A Safari Extension to take the user to the WordPress Login page for the current active tab, [hopefully] if it exists.

### On page load:

- Disable button
- If admin url already saved for this domain
    - Enable button
- else
    - If site is WordPress
        - while there are more url subdirectories
            - if siteURL + /possibleSubdirectory + /wp-admin is not a 404 page
                - Save the admin url for this domain
                - Enable button
            - break out of loop

### On button press:

- Redirect to admin url for this domain