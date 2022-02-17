# Pushing Changes Live


## Context

1. Working on store **S**.
2. Pull theme **T** (which is synced to github) from store **S**.
3. Create a dev theme from theme **T**.
4. Commit changes to git with the message, *Pulled in new changes from Shopify*.
5. Create a new fix/feature branch locally and switch to it.
6. Make changes on dev theme.
7. Changes are made to theme **T** (often by the client).


## Steps

1. Duplicate theme **T** in Shopify as a precaution.
2. Between #3 and #4 of the context:
	- Commit changes from live to main branch.
	- Create a new feature branch and switch to it.
3. Commit your work in the feature branch and switch to the main branch.
4. Pull theme **T** from Shopify.
5. Commit changes from live on main branch.
6. Merge feature branch.
7. Push to theme **T** in Shopify.
8. Push main branch to github.
