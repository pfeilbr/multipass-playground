# multipass-playground

learn [multipass](https://multipass.run/) - command line interface to launch, manage and generally fiddle about with instances of Linux

* [multipass | docs](https://multipass.run/docs)
* [Working with Multipass instances](https://multipass.run/docs/working-with-instances)

## Session

```sh
# install
brew cask install multipass

# set to use virtualbox instead of hyperkit, which is the default on macOS (ran into issues with hyperkit)
sudo multipass set local.driver=virtualbox

# launch default ubuntu instance
multipass launch

# set the primary instance.  if you don't specify the instance a command, this is the instance used
multipass set client.primary-name=capital-tapir

# list instances
multipass ls

# open shell (uses ssh under the covers)
multipass shell

# execute command and exit
multipass exec capital-tapir -- ls

# mount local host folder into instance
# /Users/pfeilbr/tmp (host) => /Users/pfeilbr/tmp (instance)
multipass mount ~/tmp capital-tapir

# unmount mounts
multipass unmount capital-tapir

# list info about instance
multipass info capital-tapir

multipass suspend capital-tapir

multipass restart capital-tapir

multipass stop capital-tapir

multipass delete capital-tapir

# purge all deleted instances permanently
multipass purge
```