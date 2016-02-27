# testCommits
This script is used to measure the performance of commits to SVN repository.

Before starting the test it would be a good idea to reset the replicator and
also delete and re-create the repository.

Parameters:

- URL               - Repository url including the repository name
- Users             - Number of users to perform commits
- UsernameBase      - See description below
- Password          - Password used to connect to the repository
- Iterations        - Number of commit iterations to perform (per user)
- ConcurrentCommits - Number of concurrent commits per user
- DirToCommit       - Name of subdir of current/working dir to commit

Make sure you have set up enough users before beginning the testing.
The usernames should be in the following format: UsernameBase1,
UsernameBase2, UsernameBase3 up to Users with the same password set.

Multiple user example:
./testCommits.sh http://10.2.5.100/svn/repo 3 user pass 10 1 30MB

For the above example there there should be 3 users set up that can access
the repository: user1, user2 and user3 with the same password "pass".

Single user example:
./concurrentCommits.sh http://10.2.5.100/svn/repo 1 user pass 10 8 30MB

In this case there should be 1 user set up: user1 with password "pass".
