Git notes
=========

##Create a Github repo using CLI 

Replace caps with custom values

    curl -u 'USER:PASS' https://api.github.com/user/repos -d '{"name":"REPO"}'
    git remote add origin git@github.com:USER/REPO.git
    git push origin master

> [Source](http://stackoverflow.com/questions/2423777/is-it-possible-to-create-a-remote-repo-on-github-from-the-cli-without-ssh)
