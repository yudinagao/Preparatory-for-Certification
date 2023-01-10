# OPerationalyze you DF

- SDK 
    - pip install azure-mgmt-datafactory
- DF service doesn't include repository for storing JSOn entities
    - not optimized for collaborationa dn version control

Azure Repos or Github
- Source control
    - track and audit changes
    - revert changes
- partial saves
- Collaborationa dn control
    - not every contributor has equal permissions
- Better CI/CD
    - configure release pipeline to triggger automatically as soons as there are any changes made to your deve factory
    -customize properties in your factory that are available as parameter in REsource Manager Template
- Better Performance
    - average factory loads 10 times faster than one authoring agaisnt the data factory service
    - resources are download via Git

Connect to a Git Repo
    - Set up Code Repository
    - Management hub
    - Version Control  
        
CI/CD
- Dev data factory created and configures with Azure Repo Git
    - all devs should have permission to author data factory resources like pipelines and data set
- devs creates a feature branch to make a change
    - they debug their pipeline runs with most recent changes
- after dev is satisfied, they create a pull request from their feature branch to the master or collaboration branch to get their change reviewed by peers
- after pull request apporved , changes are merged in the master branch, gets published to development factory
- when team is ready for deploy