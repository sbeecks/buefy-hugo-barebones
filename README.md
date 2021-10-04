# buefy-hugo-barebones
This renders a barebones [Hugo](https://gohugo.io/]) website skeleton with the modern, flexible and lightweight [Buefy](https://buefy.org/), [Bulma CSS](https://bulma.io) and [Vue.js Javascript](https://vuejs.org/) frameworks on the [Netlify cloud hosting](https://www.netlify.com/) service. 

The objective is to provide a working base for further exploration instead of building everything from scratch, with an absolute minimum of upfront learning and configuration.

The resulting Buefy components can be seen [here on Netlify](https://lucid-yonath-e15795.netlify.app/), rendering [this example code](https://buefy.org/documentation/notification) for Buefy's _Notification_ component from the [Buefy Documentation](https://buefy.org/documentation/).

## Why this is a good thing

### Why this setup
* **Hugo** is a lightning speed static site generator based on the Go language.
* **Buefy** offers lightweight UI components for Vue.js based on Bulma
* **Bulma** offers a powerful CSS framework to build responsive web interfaces.
* **Netlify** offers intuitive Git-based workflows to deploy and serve web apps.
* All these platforms are very flexible, free to use, and reasonably well documented.

### Why this repository
While Buefy, Bulma, vue.js and Hugo are well documented, the specifics of getting the basics to work can be challenging for new users of these powerful platforms. 

The idea of this repository is to provide **a simple, working starting point** for further development, while only requiring the **absolute minimal configuration** in order to get a buefy.js component served by Hugo running on Netlify. 

From this barebones starting point, it's much easier to add Hugo's powerful specifics such as blog and page templates, taxonomies, shortcodes, menus, **Markdown support**, themes, and particularly creating **multilingual pages and i18n** with Hugo, while at the same time enjoying the **simplicity**, power, and flexibility of Bulma's CSS framwork and of Buefy's **interactive UI components**.

## How to run Buefy components from Hugo on Netlify

### 10 simple steps to create a working barebone Hugo site with Buefy and Bulma on Netlify:
1. Create a project folder on your **Mac or Linux** development machine: ```mkdir ~/mySite; cd ~/mySite```
2. Create a **new Hugo site**: ```hugo new site buefy-hugo-barebones; cd buefy-hugo-barebones```
3. Ensure Hugo **renders HTML**: ```echo "\n[markup.goldmark.renderer]\n unsafe= true" >> config.toml```
4. Copy&paste a **first HTML page** with buefy components from [this file](https://github.com/sbeecks/buefy-hugo-barebones/blob/main/content/index.html) here: ```echo >> content/index.html```
5. **Check the test page** in your browser: ```hugo server -D --disableFastRender``` => live on [http://localhost:1313]().
6. **Create a repository** for the deployment on Netlify: ```git init; git add *; git commit -m 'Initial setup'```
7. Now create a new repository ```newRepo``` **on Github** (initially _without_ README.md, .gitignore and license file).
8. ... **link your repository** to GitHub: ```git remote add origin https://github.com/yourID/newRepo.git```
9. ... and **sync your files** to GitHub: ```git branch -M main; git push -u origin main```
10. Finally, [on Netlify.com](https://app.netlify.com/start), **click "create new site from Git"**, choose the GitHub repository to link from Netlify, et voilá: 
Render your web site with buefy components from Hugo on Netlify, served at a Google Page Speed of 99. It should look like [this demo site](https://lucid-yonath-e15795.netlify.app/) that is being auto-generated from this repository.

### What's next?
Well, this is the most simple way I'm aware of, with minimal configuration needs.  This does not mean it's anything close to perfect: It's just a bare skeleton.  These are a few things I suggest to explore from here:
* **Read the docs**. Move on from here. Learn using the frameworks.
* Break down the barebones ```content/index.html``` file in this repository into proper page templates (in ```layout/```) and ```.md``` Markdown files (in ```content/```). 
* Properly configure ```config.toml``` to meet your needs.
* Add necessary templates for HTML ```<head>``` directives and for the page header, navigation, and footer.
* Set up Hugo’s asset processing with Hugo pipes, in order to compress Javascript and strip unused CSS.
* Create your own page design, overriding Bulma's default styles.
* Set up forms processing on Netlify in order to receive user input from HTML forms.
* Consider separating layout and design from content files, by creating a new Hugo theme with ```hugo new theme myTheme``` and moving all page template and design files to the same-named folders in the ```themes/myTheme``` folder.
* Upgrade to Vue.js V3.0 as appropriate.
* Help improve this repository by suggesting improved configuration and documentation.
