Simple gitattributes demo
=========================

This is a simple way to show people how to use .gitattributes to maintain a personal secrets/config file, and never have it commited into git.

Steps:
=====

1. Clone the repo.
2. `./setup` (you run this as part of the cloning process, run it only once)
3. `cat config` it should contain config stuff, with "PUT_YOUR_SECRET_HERE"
4. Using your editor change "PUT_YOUR_SECRET_HERE" with "mysecret"
5. `cat config`, it'll have your secret
6. `git status`, it shows the file as modified (annoying but bare with it)
7. `git commit -av`, says "nothing to commit"... ok looking good.
8. `git archive --format=tar master > file.tar`, then unpack the tar, `cat config` within the tar and you should see "PUT_YOUR_SECRET_HERE"
9. ???
10. PROFIT
