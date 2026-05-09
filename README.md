# Graphicks Static Site Template Repository

This repository covers the basics of how to deploy a static site to production for Graphicks.

## Developer Instructions
1. Clone this repository to your local machine
2. Add your static site files to the "public" directory, including the `index.html` file of the site.
3. Commit your changes by running `git add -A` and then `git commit -m "Initial commit"`
4. Push your changes by running `git push -u origin main`
5. The site will auto-deploy when a new commit is made.

## Graphicks Deployment Instructions (Internal)
1. Create a new repository from this template using kebab-case (lowercase) for the names e.g `pelham-london`
2. Ensure the repository is set to visibility "Private"
3. Under "Start with a template" select "GraphicksStudio/static-site"
4. Login to Laravel Forge and select the `GRAPHICKS-FORGE-1` server
5. Select "New Site"
6. Enter the domain name of the site in the site name, this will be the domain the site will be used in production e.g `pelhamlondon.com`. 
7. In the aliases box, enter the name of the repository followed by `.static.graphicks.site`. For example `pelham-london.static.graphicks.site`.
8. Ensure project type of "static" is selected
9. Ensure the web-directory is set to /public as when changing to "static" it will set it to "/" by default.
10. Once the site has been created, link the GitHub repo by selecting "Git Repository" and specifying the GitHub repo.
11. Make sure to turn off "Install Composer Dependencies"
12. Ensure "Database" is left blank
13. Install The Repository
14. Go to the "Deployments" tab on the left
15. Turn on "Quick Deploy"
16. Click "Deploy Now" in the top-right

## Adding Team Members To The Organisation (Internal)
1. Go to https://github.com/orgs/GraphicksStudio
2. Select "People"
3. Invite member using their email or GitHub username.
4. Ensure the role is set to "Member"

## Adding Team Members To An Individual Site (Internal)
1. Go to the repository you would like to add the member to
2. Select "Settings"
3. Go to "Collaborators and teams"
4. Click "Add people"
5. Invite member using their email or GitHub username.
6. Select the "Write" role

## Misc Information

### Server Information

The static sites are hosted on a Digital Ocean Droplet with daily backups enabled and a reserved IP address enabled which ensures if the server goes down it can be easily replaced without having to change DNS settings.

### Cloudflare

In some scenarios, we recommend using Cloudflare for the domain nameservers and DNS particularly for sites with large images or sites with a high amount of traffic. Cloudflare offer free DDoS protection and caching to make sites run faster. They also allow instant DNS switch-over when proxying with Cloudflare.