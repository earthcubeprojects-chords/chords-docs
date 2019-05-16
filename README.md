

# Docs Repository for EarthCube CHORDS
Hello! This is our CHORDS documentation repo! This website was made to explain what CHORDS is, how to use it, and answer as many user questions as possible. It is published using GitHub Pages. We post all of our available documentation here to help use CHORDS in new and advanced ways as well as any exciting news. It was made from the Jekyll Theme [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) so if you have any questions be sure to visit his [guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/). 

## Running Locally
 If work on the documentation, you will want to develop and test on your own machine. The instructions below will get you a copy of the website up and running locally on your computer. 

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

If you have any difficulties with bundler, checkout the [bundler](https://bundler.io/) site. 

### Running Jekyll
To start the local Jekyll server:
```
bundle exec jekyll serve -watch
```
- Go to the link provided called "Server Address"
    - Ex: http://127.0.0.1:4000
- Copy and paste the IP address from the command line into the browser of your choice.
- Congratulations you are locally hosting a website for development! 
