# ScratchLatch
#### Scratch and Python bridge
----------------------------------------------
## **install**
##### ***[use command in shell]***
> pip install ScratchLatch
----------------------------------------------
## **import**
##### ***[Required on top of Python File]***
> from ScratchLatch import ScratchLatch
----------------------------------------------
## **usersession**
##### ***[creates a scratch session logging into any desired account]***
>username = "YOUR USERNAME HERE" # Enter your username in the quotes\
>password = "YOUR PASSWORD HERE" # Enter your password in the quotes\
> session = ScratchLatch(username, password) # Stores the session in 'session' variable
----------------------------------------------
## **project data**
##### ***[fetches data from desired project]***
> ID = "PROJECT ID HERE"\
> project = session.project(ID)
---
#### statistics
> data = project.stats()['loves\favorites\views\remixes'] # Stores desired project data in the 'data' variable
---
#### assets
> data = project.stats('images\sounds') # Stores desired project's images\sounds in the 'data' variable
---
#### info
> data = project.getInfo()['id\title\description\instructions\public'] # Stores desired project info in the 'data' variable
----------------------------------------------
## **project interaction**
##### ***[interactis with desired project]***
> ID = "PROJECT ID HERE"\
> projectInteraction = session.projectSession(ID)
---
#### share
> projectInteraction.share() # Shares desired project
---
#### unshare
> projectInteraction.unshare() # un-Shares desired project
---
#### love
> projectInteraction.love() # Loves desired project
---
#### favorite
> projectInteraction.share() # Favorites desired project
---
#### unlove
> projectInteraction.unlove() # un-Loves desired project
---
#### unfavorite
> projectInteraction.unfavorite() # un-Favorites desired project
---
#### remix
> projectInteraction.remix() # Remixes desired project
----------------------------------------------
## **user data**
##### ***[fetches data from desired user]***
> USERNAME = "USERNAME HERE"\
> user = session.user(USERNAME)
---
#### exists
> user.exists() # Checks if user exists
#### get messages
> user.getMessages() # Fetches user messages
#### message count
> user.messageCount() # Fetches message count
#### status
> user.getStatus() # Checks if user exists
#### bio
> user.getBio() # Checks if user exists
#### projects
> user.projects() # Fetches user projects
----------------------------------------------
## **user interaction**
##### ***[interacts with desired user]***
> USER = "USERNAME HERE"\
> userInteraction = session.userSession(USER)
---
#### follow
> userInteraction.follow() # Follows desired user
---
#### unfollow
> userInteraction.unfollow() # un-Follows desired user
---
#### toggleComments
> userInteraction.toggleCommenting() # Follows desired user
---
#### post comment
> userInteraction.postComment() # Follows desired user
----------------------------------------------
## **studio interaction**
##### ***[interacts with desired studio]***
> ID = "STUDIO ID HERE"\
> studioInteraction = session.studioSession(ID)
---
#### invite user
> inviteUsername = "USER TO ADD"\
> studioInteraction.invite(inviteUsername) # Invites desired user to studio
---
#### add project
> projectID = "PROJECT TO ADD"\
> studioInteraction.addProject(projectID) # Adds desired project to studio
---
#### post comment
> comment = "THIS IS A COMMENT SENT FROM PYTHON!"\
> studioInteraction.postComment(comment) # Posts comment to desired studio
---
#### get comments
> limit = 10\
> studioInteraction.getComments(limit=limit) # Gets last 10 comments posted in desired studio
---
#### follow
> studioInteraction.follow() # Follows desired studio
---
#### unfollow
> studioInteraction.unfollow() # un-Follows desired studio
----------------------------------------------
# Cloud Variables
> ID = "PROJECT ID HERE"\
> cloud = session.cloud()
----------------------------------------------
## **Scratch**
> scratchCloud = cloud.scratch(ID)
---
#### set variable
> scratchCloud.setVar("VARIABLE NAME", "VARIABLE VALUE")
---
#### get variable
> scratchCloud.getVar("VARIABLE NAME")
---
## **Turbowarp**
> turbowarpCloud = cloud.turbowarp(ID)
---
#### set variable
> turbowarpCloud.setVar("VARIABLE NAME", "VARIABLE VALUE")
---
#### get variable
> turbowarpCloud.getVar("VARIABLE NAME")
----------------------------------------------

