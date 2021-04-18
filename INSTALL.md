# Local Installation

## Install node with homebrew
1. Install [Homebrew](https://brew.sh/)
1. Install Node: `$ brew install node`
1. Create a dltlandscape directory: `$ mkdir dltlandscape`
1. Switch to dltlandscape directory: `$ cd dltlandscape`
1. Clone the landscape app: `$ git clone git@github.com:cncf/landscapeapp.git`
1. Setup the landscape app: `$ cd landscapeapp`
1. `$ npm install -g yarn@latest`
1. `$ yarn`
1. `$ cd ../`
1. Clone the dlt-landscape: `$ git clone git@github.com:dltlandscape/dlt-landscape.git`
1. Add the following to your .zshrc or .bashrc updating the directory paths for your local setup:

    ```
    function y { export PROJECT_PATH=`pwd` && (cd ../landscapeapp && yarn run "$@")}
    export -f y
    # yf does a normal build and full test run
    alias yf='y fetch'
    alias yl='y check-links'
    alias yq='y remove-quotes'
    # yp does a build and then opens up the landscape in your browser ( can view the PDF and PNG files )
    alias yp='y build && y open:dist'
    # yo does a quick build and opens up the landscape in your browser
    alias yo='y open:src'
    alias a='for path in /Users/user/dltlandscape/{landscapeapp,finos-landscape}; do echo $path; git -C $path pull -p; done; (cd /Users/user/dltlandscape/landscapeapp && yarn);'
    ```
1. Source your bashrc or zshrc, for example: `$ source ~/.zshrc` or open a new terminal window.
1. Got to the dlt-landscape directory` $cd dlt-landscape`
1. You can now use the alias you added earlier to run a local version of the app. 
1. First use `yf` to fetch all the data. If this fails you'll need to set the Crunchbase key as an ENV VAR like `$export CRUNCHBASE_KEY_4=yourkeydata`
1. You can then run a quick build and open a local server at localhost:3000 with `$ yo` or a production build with `yf`

