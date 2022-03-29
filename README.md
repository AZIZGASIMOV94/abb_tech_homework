0. Register on the GitHub and create a remote git repo
$ mkdir abb_tech_task_1
$ git clone https://github.com/AZIZGASIMOV94/abb_tech_homework.git
$ cd abb_tech_task_1
$ git config --global user.name "AZIZGASIMOV94"
$ git config --global user.email gasimovaziz@gmail.com 
$ git add readme.md


1. Stashing in git (git stash):
a) make some changes in your repo and save them to stash area
b) check repo status
c) restore saved data from stash area
d) check repo status


2. Understand merging strategies (fast-forward, recursive etc)

In a few words describe each strategy

modification for feature_a branch 
=======


some modification in branch b

Git Flow
In the Git flow development model, you have one main development branch with strict access to it. It’s often called the develop branch.

Developers create feature branches from this main branch and work on them. Once they are done, they create pull requests. In pull requests, other developers comment on changes and may have discussions, often quite lengthy ones.

It takes some time to agree on a final version of changes. Once it’s agreed upon, the pull request is accepted and merged to the main branch. Once it’s decided that the main branch has reached enough maturity to be released, a separate branch is created to prepare the final version. The application from this branch is tested and bug fixes are applied up to the moment that it’s ready to be published to final users. Once that is done, we merge the final product to the master branch and tag it with the release version. In the meantime, new features can be developed on the develop branch.

Below, you can see Git flow diagram, depicting a general workflow:

Git flow Diagram depicging general workflow
One of the advantages of Git flow is strict control. Only authorized developers can approve changes after looking at them closely. It ensures code quality and helps eliminate bugs early.

However, you need to remember that it can also be a huge disadvantage. It creates a funnel slowing down software development. If speed is your primary concern, then it might be a serious problem. Features developed separately can create long-living branches that might be hard to combine with the main project.

What’s more, pull requests focus code review solely on new code. Instead of looking at code as a whole and working to improve it as such, they check only newly introduced changes. In some cases, they might lead to premature optimization since it’s always possible to implement something to perform faster.

Moreover, pull requests might lead to extensive micromanagement, where the lead developer literally manages every single line of code. If you have experienced developers you can trust, they can handle it, but you might be wasting their time and skills. It can also severely de-motivate developers.




-----
Trunk-based Development Workflow
In the trunk-based development model, all developers work on a single branch with open access to it. Often it’s simply the master branch. They commit code to it and run it. It’s super simple.

In some cases, they create short-lived feature branches. Once code on their branch compiles and passess all tests, they merge it straight to master. It ensures that development is truly continuous and prevents developers from creating merge conflicts that are difficult to resolve.

Let’s have a look at trunk-based development workflow.

Trunk-based development diagram
The only way to review code in such an approach is to do full source code review. Usually, lengthy discussions are limited. No one has strict control over what is being modified in the source code base—that is why it’s important to have enforceable code style in place. Developers that work in such style should be experienced so that you know they won’t lower source code quality.

This style of work can be great when you work with a team of seasoned software developers. It enables them to introduce new improvements quickly and without unnecessary bureaucracy. It also shows them that you trust them, since they can introduce code straight into the master branch. Developers in this workflow are very autonomous—they are delivering directly and are checked on final results in the working product. There is definitely much less micromanagement and possibility for office politics in this method.

If, on the other hand, you do not have a seasoned team or you don’t trust them for some reason, you shouldn’t go with this method—you should choose Git flow instead. It will save you unnecessary worries.

---link: https://www.toptal.com/software/trunk-based-development-git-flow
---link: https://betterprogramming.pub/differences-between-git-merge-and-rebase-and-why-you-should-care-ae41d96237b6

