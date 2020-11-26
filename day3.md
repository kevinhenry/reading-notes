Revisions in the Cloud

Git Intro

VCS - Version Contol System allows us to revisit various versions of a file or set of files. It records changes. Version control enables us to revert a file or project to a previous version. The best thing about Version Control is that mistakes with files can easily be rectified.

There are Local Version Control, Centralized Version Control, and Distributed Version Control.

Local Version Control - one database on a your hard disk that stores all of the changes to files

Centralized Version Control - single server storing all changes and file versions to be acceed by various clients

Distributed Version Control - allowas multiple mirrored respositiories


Git vs. Github - 

Git is a Distributed Version Control System made up of snapshots. Git acts as a gatekeeper and will always detect file corruption or loss of information in transit

Github is a hub-focused tool which facilitates interation-manager workflow. It is the largest host for Git repositories and is used by millions of developers worldwide.

local vs remote

local repository structure has a working directory, index, and head.

remote repositories are versions of a project that are hosted on the Internet or network somewhere.

clone - create a duplicate of an existing Git repository

$ git clone https://github.com/test


commit - after staging one or multiple filees, you commit changes along with a message about what you did.

$ git commit -m "made change x,y,z"


ACP - Add, commit, push. this is the order of operations for git.

deployment - a request to deploy a specific ref (branch, SHA, tag)