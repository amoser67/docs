
# Theme Development Instructions


## Requirements

1. There is an existing plugdigital github repo associated with the store you are working on. If this is not the case, use the instructions for setting up a theme repo to create one.

2. Admin access to the store.

3. SSH access to both a personal GitHub repo and the plugdigital GitHub repo.

4. Shopify CLI is installed globally.



## Steps

1. Clone the repository.
  - If you have never cloned the repo onto your local machine:
    - `$ git clone git@github.com:plugdigital/[repository-name].git`
    - `$ cd [repository-name]`
  - Otherwise update your local copy:
    - Navigate to your local copy of the repository.
    - `$ git checkout main`
    - `$ git pull origin main`


2. Create a new branch, prefacing the name with fix/ or feature/ based on your current task.
  - `$ git checkout -b feature/add-rating-to-product-cards`


4. Log in to the store you will be working on.
  - `$ shopify login --store=[store-name]`


5. Start a development server to start working on the theme.
  - `$ cd theme`
  - `$ shopify theme serve --live-reload=[hot-reload/full-page/off]`


6. When you have finished your current task, copy the theme preview link that is printed to the terminal when running the `shopify theme serve` command, and give it to the product manager.


7. Once the project manager has approved your changes, upload your feature/fix branch to GitHub so that the lead developer of the project can review it.
  - Navigate to the project directory.
  - `$ git add .`
  - `$ git commit -m "Describe what feature you added or bug you fixed here."`
  - `$ git push origin feature/add-rating-to-product-cards`


8. If the review process in step 5 or step 6 determines that changes need to be made to your code, make the changes and start over from step 5.


9. Once the review process is complete, the lead project of the project will be responsible for merging your changes into the main branch, as well as updating the live theme. See *docs/pushing-changes-live.md*.
