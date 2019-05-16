# Documentation Repository for EarthCube CHORDS

_Shortcut: See the CHORDS [published documentation](https://earthcubeprojects-chords.github.io/chords-docs/)._

Hello! This is our CHORDS documentation repository! The content explains what CHORDS is, how to use use it in new and advanced ways, answer as many user questions as possible, and post any exciting news.

The website is published using GitHub Pages, and runs on the Jekyll framework, using the Jekyll [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) Theme. If you have any questions about the framework, be sure to visit the [Minimal Mistakes guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/). 

## Running Locally
 If you want to work on the documentation, you will develop and test on your own machine. The instructions below will get a copy of the website up and running locally on your computer. 

### Prerequisites
- Install the latest version of Ruby. On OSX, this is:
```
$ brew install ruby
```
Visual Studio Code

- Clone this repository, and navigate to it:
```
git clone https://github.com/earthcubeprojects-chords/chords-docs.git
cd chords-docs
```
- Update the gems:
```
gem update
```
- Install the gems:
```
bundle install
```
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
