# Docs Branch, Chords Website
Hello! This is our CHORDS website repo! This website was made to explain what CHORDS is, how to use it, and answer as many user questions as possible. We post all of our available documentation here to help use CHORDS in new and advanced ways as well as any exciting news. It was made from the Jekyll Theme [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) so if you have any questions be sure to visit his [guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/). 

## Getting Started
 The instructions below will get you a copy of the website up and running locally on your computer. 

### Prerequisites
The latest version of Ruby
```
$ brew install ruby
```
Visual Studio Code 


### Running Locally
- Clone the repository locally
- Navigate to your repo with terminal or command line
- make sure gems and ruby have been updated!
```
gem update
```
- Install bundler
```
bundle install
```
- Type "bundle" in your command line to update gems
- Update the theme by running 
```
bundle update
```

If you have any difficulties with bundler checkout the [bundler](https://bundler.io/) site. 

- once you've got bundler installed and updated type 
```
bundle exec jekyll serve
```
- Go to the link provided called "Server Address"
    - Ex: http://127.0.0.1:4000
- if you want to update the website in real time type 
```
bundle exec jekyll serve --watch
```
- Copy and paste the IP address from the command line into the browser of your choice.
- Congratulations you are locally hosting a website in development! 
