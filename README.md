# Documentation Repository for EarthCube CHORDS

_Shortcut: See the CHORDS [published documentation](https://earthcubeprojects-chords.github.io/chords-docs/)_

Hello! This is our CHORDS documentation repository! It explains what CHORDS is, how to use it, and answer as many user questions as possible. It is published using GitHub Pages. We post all of our available documentation here to help use CHORDS in new and advanced ways as well as any exciting news. 

The website is run on the Jekyll framework, using the Jekyll [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Theme, so if you have any questions be sure to visit his [guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/). 

## Running Locally
 If you want to work on the documentation, you will develop and test on your own machine. The instructions below will get a copy of the website up and running locally on your computer. 

### Prerequisites
- Install the latest version of Ruby. On OSX, this is:
```
$ brew install ruby
```
Visual Studio Code

- Clone this repository, and navigate to it in a terminal.
- Update the gems:
```
gem update
```
- Install the gems:
```
bundle install
```
- Type "bundle" in your command line to update gems
- Update the theme by running 
```
bundle update
```

If you have any difficulties with bundler, see the [bundler](https://bundler.io/) site. 

### Running Jekyll
To start the local Jekyll server:
```
bundle exec jekyll serve -watch
```
- Copy and paste the IP address from the command line into the browser of your choice.
    - Ex: http://127.0.0.1:4000
- Congratulations you are locally hosting a website for development! 

The _-watch_ switch causes Jekyll to update the local website anytime you save the edits to a file; a very handy way to instantly see your changes. Jowever, if you change stylesheets or javascript, you will need to clear your browser cache and reload the page.
