# heroku-buildpack-root-monorepo

This buildpack accomplishes three things:
1. Modules in marketing-sites use relative paths pointing to where they expect `modules` to be (in the root of the repository). So first this buildpack sets up a folder structure to account for this.
2. It copies the Procfile to where Heroku expects it to be.
3. It removes unneeded files to cut down on Heroku slug size.

This buildpack is meant to be listed after the Node buildpack in your Heroku buildpacks list.

