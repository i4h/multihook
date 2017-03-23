# Multihook

A very simle script, that will delegate running any git hook to 
a number of ''sub-hooks'' saved in the right directory.

Similar code can be found here:
- https://github.com/metajack/multihook
- https://gist.github.com/carlos-jenkins/89da9dcf9e0d528ac978311938aade43

If you are looking for a simple bash solution, this one might be useful.

## Installing Multihook

To use multihook in place any git hook, download the script to the right place
(WARNING: this will overwrite an existing hook).

````
hook="pre-commit";
cd /to/your/repository
curl -o .git/hooks/$hook  https://raw.githubusercontent.com/i4h/multihook/master/multihook && chmod ug+x .git/hooks/$hook && mkdir .git/hooks/$hook.d
````

## Installing hooks

Multihook will look for hooks in `.git/hooks/hook-name.d/`. To install a new hook, copy it into the corresponding directory.
For example, to install a pre-commit hook:

````
cp ~/my_hooks/some_hook .git/hooks/pre-commit.d/
````





