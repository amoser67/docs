
# Instructions for Setting Up a Store's Repository


## Requirements

- Shopify CLI.
- git, version >= 2.3.
- Unix based OS (if using Windows, should be easy enough to convert the instructions).
- SSH access to the plugdigital GitHub organization.
- Admin access to the store.


## Steps

1. Create a directory for the project, and navigate to it (replacing *example-store* with the store name).
	- `$ mkdir example-store`
	- `$ cd example-store`
2. Initialize an empty git repository for the project.
	- `$ git init -b main`
3. Clone an existing theme as a starting point, renaming the directory *theme*.
	- If cloning a theme from a theme repo:
		- `$ git clone https://github.com/Shopify/dawn.git theme`
		- `$ sudo rm -r theme/.git; sudo rm -r theme/.github`
	- If starting with a theme currently on the client's store:
	 	- `$ mkdir theme`
	 	- `$ cd theme`
		- `$ shopify theme pull`
		- `$ cd ..`
4. Go to GitHub and create a new repository in the plugdigital organization, named *example-store*.
5. Make the initial commit and then connect the local project repository to the remote repository.
	- `$ git add .`
	- `$ git commit -m "First Commit"`
	- `$ git remote add origin git@github.com:plugdigital/example-store.git`
	- `$ git push origin main`
6. Create a repository in the theme directory.
	- `$ cd theme`
	- `$ git init -b theme`
	- `$ git add .`
	- `$ git commit -m "First Commit"`
7. Now connect the theme directory to the remote repository', but on its own branch named *theme*.'
	- `$ git remote add origin git@github.com:plugdigital/example-store.git`
	- `$ git push origin theme`
8. Now go to *example-store.myshopify.com/admin/themes*, click ***Add theme*** > ***Connect from GitHub***, and follow the provided instructions to connect to the *plugdigital/example-store* repository's *theme* branch. You may need someone with administrative access to the plugdigital GitHub organization to approve this connection. If so, repeat step 8 once it has been approved.


### Additional Notes
- The only entity that should push or pull from the *theme* branch is Shopify itself. If we want to push or pull a theme, we will do so using Shopify CLI.
- The *example-store* repo's *main* branch is where our commits should be made, and will contain the unpackaged JS and CSS source code (as well as the theme directory).
- It shouldn't be assumed that the theme subdirectory on the *main* branch is up to date with the published theme (but it will generally be close), that is what the *theme* branch is for.
- Example repo: https://github.com/plugdigital/plug-dev-11-sandbox
