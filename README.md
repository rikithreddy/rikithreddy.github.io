# My Personal Page

How to get running on your local linux machine


## Install dependencies

Jekyll depends on Ruby run the following command to install the dependency

`sudo apt-get install ruby-full build-essential`



# Configure Gem Environment for your user account

Paste the essentials in .bashrc which would help keep gem settings each time 

`echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME=$HOME/gems' >> ~/.bashrc
echo 'export PATH=$HOME/gems/bin:$PATH' >> ~/.bashrc
source ~/.bashrc`


# Install Jeykll
Run the following command to install jekyll on your machine

`gem install jekyll bundler`
