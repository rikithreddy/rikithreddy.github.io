# My Personal Page

This repo contains the source code for my personal github pages you can install it on your machine following the below instructions



## How to install on your personal machine

How to get running on your local linux machine


### Install dependencies

Jekyll depends on Ruby run the following command to install the dependency

`sudo apt-get install ruby-full build-essential`



### Configure Gem Environment for your user account

Paste the essentials in .bashrc which would help keep gem settings each time 

`echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc`

`echo 'export GEM_HOME=$HOME/gems' >> ~/.bashrc`

`echo 'export PATH=$HOME/gems/bin:$PATH' >> ~/.bashrc`

`source ~/.bashrc`


### Install Jeykll
Run the following command to install jekyll on your machine

`gem install jekyll bundler`



### Setup github pages

Run the following command to install all other dependencies which will be required for running the app

`cd /path/to/repo/`
`bundle install`

### Running Application 

To start the jekyll server run the following command

`bundle exec jekyll serve`
