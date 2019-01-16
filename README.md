# Heroku buildpack for multiple package.json files

Heroku applications assume one repo to one application.

Given a single repo with multiple applications in it, this buildpack provides the ability to specify the package.json for each application.

# Usage

1. Create a package.json for each application in your repo
2. Create a bunch of Heroku apps.
3. For each app, set `PACKAGE_JSON=relative_path_to_package/package.json` 

4. Add the buildpack from the command line or via the UI
   `heroku buildpacks:add -a <app> https://github.com/klall/heroku-buildpack-multi-package.json.git`
4. For each app, `git push git@heroku.com:<app> master`
