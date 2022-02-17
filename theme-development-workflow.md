
# Theme Development Instructions

[< All Docs](https://amoser67.github.io/docs/)

## Requirements

1. There is an existing plugdigital GitHub repo associated with the store you are working on, and there is a theme in the store which is synced to that repo. For instructions on how to set up a repo and connect it to a theme, see [Setting Up a Store's Repository](https://amoser67.github.io/docs/setting-up-a-stores-repository).
2. Admin access to the store.
3. SSH access to the plugdigital GitHub repo.
4. Shopify CLI installed globally.


## Steps

1. Clone the repository.
    - If you have never cloned the repo onto your local machine:
      - `$ git clone git@github.com:plugdigital/[repository-name].git`
      - `$ cd [repository-name]`
    - Otherwise update your local copy:
      - Navigate to your local copy of the repository.
      - `$ git checkout main`
      - `$ git pull origin main`
2. Update your copy of the main branch with changes from the live site.
    - `$ cd theme`
    - `$ shopify theme pull`
    - Select the theme from the list printed to the terminal.
    - `$ cd ..`
    - `$ git add .`
    - `$ git commit -m 'Pulled in updates from Shopify.'`
2. Create a new branch, prefacing the name with fix/ or feature/ based on your current task.
    - `$ git checkout -b feature/add-rating-to-product-cards`
4. Log in to the store you will be working on.
    - `$ shopify login --store=[store-name]`
5. Start a development server to begin working on the theme.
    - `$ cd theme`
    - `$ shopify theme serve --live-reload=[hot-reload/full-page/off]`
6. When you have finished your current task, copy the theme preview link that is printed to the terminal when running the `shopify theme serve` command, and give it to the appropriate project manager for review.
7. Once the project manager has approved your changes, upload your feature/fix branch to GitHub so that the developer in charge of the project can review it.
    - Navigate to the project directory.
    - `$ git add .`
    - `$ git commit -m "Describe what feature you added or bug you fixed here."`
    - `$ git push origin feature/add-rating-to-product-cards`
8. If the review process in steps 6 or 7 determines that changes need to be made to your code, make the changes and start over from step 6.
9. Once the review process is complete, the developer in charge of the project will be responsible for merging your changes into the main branch, as well as updating the live theme. If you are the developer in charge, see [Pushing Changes Live](https://amoser67.github.io/docs/pushing-changes-live).
