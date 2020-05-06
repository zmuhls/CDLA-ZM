# Export Saved Reddit Posts

[![Build Status](https://travis-ci.org/csu/export-saved-reddit.svg?branch=master)](https://travis-ci.org/csu/export-saved-reddit) [![Code Coverage](https://img.shields.io/codecov/c/github/csu/export-saved-reddit.svg)](https://codecov.io/gh/csu/export-saved-reddit)

Exports saved and/or upvoted Reddit posts into a HTML file that is ready to be imported into Google Chrome. Sorts items into folders by subreddit.

## Requirements
* [Python 3.x](https://www.python.org/downloads/)
* [pip](https://pip.pypa.io/en/stable/installing/)
* [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) (recommended) 

## Installation
First, make sure you have [Python 3.x](https://www.python.org/downloads/), [pip](https://pip.pypa.io/en/stable/installing/), and [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) installed on your machine.

Run the following in your command prompt to install:

    git clone https://github.com/csu/export-saved-reddit.git
    cd export-saved-reddit
    pip install -r requirements.txt

To install without git, [download the source code from GitHub](https://github.com/csu/export-saved-reddit/archive/master.zip), extract the archive, and follow the steps above beginning from the second line.

## Usage
1. [Make a new Reddit](https://www.reddit.com/prefs/apps) app to get a `client id` and a `client secret`.

    - Scroll to the bottom of the page and click "create app"
    - You can name the app anything (e.g. "export-saved"). Select the "script" option. Put anything for the redirect URI (e.g. https://christopher.su).
    - After creating the app, the client id will appear under the app name while the client secret will be labeled "secret".

    ![](https://i.imgur.com/zQZUEuB.png)

2. In the `export-saved-reddit` folder, rename the `AccountDetails.py.example` file to `AccountDetails.py`.
3. Open the `AccountDetails.py` in a text editor and enter your Reddit username, password, client id, client secret within the corresponding quotation marks. Save and close the file.
4. Back in your shell, run `python export_saved.py` in the `export-saved-reddit` folder. This will run the export, which will create `chrome-bookmarks.html` and `export-saved.csv` files containing your data in the same folder.

### Additional Options
    usage: export_saved.py [-h] [-u USERNAME] [-p PASSWORD] [-id CLIENT_ID]
                           [-s CLIENT_SECRET] [-v] [-up] [-all] [-V]
    
    Exports saved Reddit posts into a HTML file that is ready to be imported into
    Google Chrome or Firefox
    
    optional arguments:
      -h, --help            show this help message and exit
      -u USERNAME, --username USERNAME
                            pass in username as argument
      -p PASSWORD, --password PASSWORD
                            pass in password as argument
      -id CLIENT_ID, --client-id CLIENT_ID
                            pass in client id as argument
      -s CLIENT_SECRET, --client-secret CLIENT_SECRET
                            pass in client secret as argument
      -v, --verbose         increase output verbosity (deprecated; doesn't do
                            anything now)
      -up, --upvoted        get upvoted posts instead of saved posts
      -all, --all           get upvoted, saved, comments and submissions
      -V, --version         get program version.

## Updating
To update the script to the latest version, enter the `export-saved-reddit` folder in your shell/command prompt and enter the following:

    git pull

## Help
If you have any questions or comments, please [open an issue on GitHub](https://github.com/csu/export-saved-reddit/issues).

## [Contributing](https://github.com/csu/export-saved-reddit/blob/master/CONTRIBUTORS.md)

If you would like to contribute, check out the project's [open issues](https://github.com/csu/export-saved-reddit/issues). [Pull requests](https://github.com/csu/export-saved-reddit/pulls) are welcome.
