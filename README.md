# EduVaultAI Odyssey Blog
## Installation Instructions
- MacOS: https://gohugo.io/installation/macos/
- Windows: https://gohugo.io/installation/windows/

### Summary
1. Install Hugo prerequisites: Git, Go, Dart Sass
2. Install Hugo: `CGO_ENABLED=1 go install -tags extended,withdeploy github.com/gohugoio/hugo@latest`  
**For Windows, use this command in step 2:**  
`set CGO_ENABLED=1 && go install -tags extended,withdeploy github.com/gohugoio/hugo@latest`
## Running Hugo Static Site Server
https://gohugo.io/getting-started/quick-start/

Running the site locally in draft mode (i.e. shows all `draft: true` posts)
```bash
hugo server -D
```

## Creating a post
```bash
hugo new posts/name-of-post-like-these.md
```
Also note that Hugo does not like the pages to be created while running. So stop and then run the above command. Rerunning with:
```bash
hugo server -D --ignoreCache
```
might help.

If removing a post run this afterwards to clean directories:
```bash
hugo --cleanDestinationDir
```

## Before pushing...
To prepare for deployment to `main`:
```bash
hugo --cleanDestinationDir # in order to clear the public/ directory.
hugo # to rebuild without drafts.
```

## Deploying the Site
### Configuration
Make the following changes:
- Set the baseURL for your production site. This value must begin with the protocol and end with a slash, as shown above.
- Set the languageCode to your language and region.
- Set the title for your production site.

### Publish
When you publish your site, Hugo creates the entire static site in the public directory in the root of your project. This includes the HTML files, and assets such as images, CSS files, and JavaScript files.

When you publish your site, you typically do not want to include draft, future, or expired content. The command is simple.

### To Github Pages.
https://gohugo.io/hosting-and-deployment/hosting-on-github/

### Customizations doc
https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-features

## Themes + Packages
Theme: https://github.com/adityatelange/hugo-PaperMod
Comments via Github Discussions: https://giscus.app