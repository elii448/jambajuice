# [ Valheim - "jambajuice" World Files ]

## Valheim file


**`Disclaimer`**

 * DO NOT RENAME THE FILES
 * ALWAYS UPDATE THE LOCAL REFERENCE OF THE REPOSITORY AFTER HOSTING
 * BACUP THE WORLD EVERY PLAY SESSION IN YOU SEPARATE LOCAL FILE

**`Definitions`**
 * Always replace with MM-DD-YYYY with current date
 * When doing git commands, make sure you have navigated the git folder in your machine.
   * Check letter A, number 1, first to second bullet to navigate to your folder.

# A. Getting started with Git

 `PREREQUISITES:`
 * install `git` in your pc. Just follow the installation wizard.
 * The installation usually includes `Git Bash`, but if it did not, should install it too.
 * Once done, you may check the installation by running `git` command in `Git Bash`. It will show you some commands you can do with `git` if the installation was successful.
 * If incase, no sample commands show and `command not found` appears, just restart your machine to complete the installation.

 1.) To begin, open Git Bash. You must clone this link: `https://github.com/elii448/jambajuice` to your desired location. Then checkout `main` branch
   * Terminal commands:
     * `cd d:`
     * `cd *desired location*` -> eg. `cd Games/Valheim\ worlds/`
     * `git clone https://github.com/elii448/jambajuice`
     * `cd jambajuice`
     * `git checkout main`

# B. Copying the shared world

 1.) Copy the `.db` & `.fwl` files from the local git repository in the jambajuice folder

 2.) Place them in your Valheim wolrds directory
 * Default: `%userprofile%\AppData\LocalLow\IronGate\Valheim\worlds`
   * eg: `C:\Users\popoy\AppData\LocalLow\IronGate\Valheim\worlds`

 3.) If done correctly, you should be able to see the world once you start-up the game

# C. Hosting a session
 1.) Let the other players know you'll be hosting by sending a message on discord or messenger.

 2.) Update your local world version by following the stemps in "`A. Copying the shared world`"

 3.) Make sure to tick the `Start Server` & `Community Server` boxes before starting

 `NOTE:` Make sure to add a password

# C. Ending The Play Session 

 1.) Make sure everyone logs out before you 

 2.) Logout & exit Valheim completely

 `NOTE:` To be safe, wait for `5 ~ 10 minutes` after closing the game before proceeding to the next steop to make sure the game is done writing the changes to the wolrd files.

 3.) From `main` branch, branch out to `progress-MM-DD-YYYY` (currrent date)
   * eg: `progress-02-16-2020`
   * Terminal commands:
     * `git checkout -b progress-02-16-2020`

   **`How to branch out:`**
   * open your `terminal` or `command line` (cmd)
   * navigate to your git directory
   * `git checkout -b progress-MM-DD-YYYY` -> replace with MM-DD-YYYY with current date

 4.) Copy the `.db` (`Data Base File`) & `.fwl` to the repository folder after wrapping up the play session.

 `OPTIONAL:` Update the contents of the `Backup` folder as well.

 5.) Commit and push the new files
   
   **`How to commit and push`**

   * a.) `git add --all`
   * b.) `git commit -m "game progress as of MM-DD-YYYY played in the afternoon"`
   * c.) `git push -u origin progress-MM-DD-YYYY`

 6.) Merge the latest progress to `main` branch

   **`How to merge`**

   * a.) `git checkout main`
   * b.) `git pull origin progress-MM-DD-YYYY`
   * c.)
     * **`Conflict scenario:`**
       * A word conflict may appear in your terminal. When this happens, delete all the files in the `game_file` folder, then paste the latest game file again from the Valheim worlds folder.
       * Default: `%userprofile%\AppData\LocalLow\IronGate\Valheim\worlds`
       * follow letter C number 5 `How to commit and push`, first and second bullet
     * **`With or without conflicts`**
       * With or witout conflicts you must push this merge
       * `git push`



