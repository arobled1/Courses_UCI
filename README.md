# Courses_UCI
Graduate Courses taken at the University of California, Irvine. 

# Chemisty 237: Mathematical Methods in Chemistry
Graduate Course covering both analytic and numerical methods commonly used in theoretical chemistry and physics.

## Github Crashcourse
Github is a tool for source control (tracking a document in time, saving all versions and changes made to that document), and for collaborating and developing projects with other people.

To contribute to the project just read the example work-flow provided below (there are fancier things you can learn/read about using Git/Github, but all the essentials are covered below).

Please note: The tutorial below will assume you have the Mac OS.
If you are using a different Operating System the idea is the same (all of the git commands are the same), but you will need to look up your specific operating system install process (windows people may want to look into git bash).

#### Github Install
(Does not depend on your operating system).
To get started you will need to make a `Github` account; Please Note: most people see/use Github as a professional tool.
Remember that when making your account.
You may find Github to be a useful tool and continue to use it in the future.
If you use a name.edu email you will get access to some extra tools in Github which  may be useful in your future developments.

To make an account head over to the [GitHub](http://github.com) website and follow thier directions.
With your new github account you have access to the tools of Github, the online repository functionality.
However, you are not going to be working online, you will want to work on your local machine (your laptop).
To do this we need the second half of the software, known as `git`.

#### Git Install
(Will depend on your operating system: windows and linux do not use Xcode).
On mac git will actually come installed on your device.
It will be an older version of git and you should really get the most recent version.
To do this you are going to need Xcode and the Xcode command line tools, on mac you can follow the [Xcode](https://github.com/swflynn/fortran_tutorials/tree/master/fortran_crashcourse/00) install section here (Note: Just scroll down to the Xcode install section, you do not need anything else).

Now that you have Xcode on your machine you can go download [Git](https://git-scm.com/downloads).
Run the dmg file and follow the prompts to get Git.
Once the install is done type the following into your terminal to make sure everything worked (do not type $, it just implies to be typed into terminal).

`git --version`

Now that you have a working version of git you will want to set-up your username and email address on your laptop.
I would suggest using the same name and password as you used on Github since we are going to be using these accounts together.

`$ git config --global user.name "your name here"`

`$ git config --global user.email "your_name@domain.ext"`

With this done you should now have both a Github account (on the internet) and a Git account (on your local device).
Remember, we use the git account on our local machine to develop material, we then pass that to the Github account on the internet for everyone to use.

#### Git and Github Workflow
As you can see I have already made a Github Repo for the Course, so you will just need to copy it, make changes, and add them back to here.

To copy it we are going to make a `fork`.
This will make a copy of my (swflynn) Chem 237 repo onto your Github page (remember swflynn owns this page, you cannot make changes directly to it, but you can change your own Github account).
To do this, go to the top-right corner of the page (swflynn/Courses_UCI) and click on the `Fork` button.
This will now make a new  version of Courses_UCI on your github account (name/Courses_UCI).
You can now edit YOUR version of the course,  and work with it on your local machine.

I suggest making a directory on your local machine for ALL of your Github projects (this is just a suggestion).
To do this make a directory somewhere on your computer, you can name it whatever you want (`$ mkdir ~/Desktop/github`) is an example.
Move to this directory, and inside it we are going to make a copy of the Chem237 Repo.
To do that use the following command

`$ git clone "url"`

Replace "url" with the url found on the forked (your) version of Courses_UCI repo under the green tab called `Clone or Download`
After this runs you should see all of the resources from the Github on your local machine.

Don't get confused, you have now taken a copy of the Course owned by (swflynn) for yourself and placed it in on your Github.
You then took your personal copy from Github, and made a version on our local machine for Git.

Now, the version owned by swflynn is going to be changing (everyone will be copying it making changes, and then adding them back).
We want to be up-to-date with swflynn.
The copy owned by swflynn is `upstream` i.e. it is farther behind because it is the original, and your copy is called `downstream` (because you are making changes).
We need the upstream copy to be a `remote`, the directory we  watch, copy, and merge  with.

Because the original repo (owned by swflynn) will be constantly changing as everyone develops and adds material we need to be sure we stay up-to-date.
To see what repositores are remotes try `$ git remote -v`.
This should show YOUR version of the course (not swflynn).
We need to add the original upstream (owned by swflynn) to this list.
To do this go into the Courses_UCI directory (locally) and type the following:

`$ git remote add upstream "the url from swflynn page under copy / download"`.

If you try the remote command again you should now see both your github version and the version owned by swflynn.

Now that we have linked both your Github page and the original swflynn github page to your Git account we can start developing.
You need to make sure you are up-to-date, before you start changing your local version check to see if you are up-to-date with swflynn.

To do this, (everytime you plan to work locally) you should fetch the swflynn online repo and merge to your git).
This is done with the following command:

`$ git pull upstream master`

Now that you have an up-to-date version of the local repo, you need to update your github. To do this, type the following:

`$ git push`

Now your local and github are in sync and you are ready to develop.

Open files, edit them, do whatever you want (Remember it is impossible to 'break' anything this is all your local version).

Once you have made some changes  and want to save them type the following command

`$ git status`

This shows you all changes that you have made from the previously saved version of the repo (on your local account).

To save all the changes you will need to tell git.
A simple way to do this in one step is the following

`$ git add .`

Which will add all changes to be saved.

Finally we need to commit to saving these changes.
This is done using

`$git commit -m "add a brief message summarizing changes"`

The message should be short and informative, i.e. (update lecture 2 notes).

With this done we have now saved our changes to the repo!
Remember, these changes are all to your local git account.
The next step is to push these changes to your (not swflynn) Github account for the world to see!

`$ git push`

If this does not work for some reason (your configuration is not  set up correct) you can also try

`$ git push origin master`

Which tells git to push to the master copy on your Github (the main version).

Now that you have saved changes you are happy with, you should update the original version owned by swflynn.
To do this, go to your Github repo for the course and select Create New Pull Request.
As long as everything checks out you should get a green message and submit the pull request.
swflynn will need to review your changes and add them to the original account.
Please see the [Official](https://help.github.com/articles/creating-a-pull-request-from-a-fork/) Giithub guide if you are confused.

This is it you are now a fully-functioning member of the Git/Github community.
If you are confused, or experience any issues during this process please do not hesitate to contact me.
This project is for everyone, do not let this workflow stop you from contributing!

