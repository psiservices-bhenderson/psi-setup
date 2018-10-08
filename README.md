At PSI our account needs to be prefixed with psiservices-. Which effectively
means we need a separate account from our personal account. I balked at it
originally, but I didn't have a good argument. Setting it up, I want to be able
to contribute to non-psi repositories using my personal account. This means
setting up my local computer to use multiple ssh keys. The recommendations
online was to setup different hosts in .ssh/config. I initially tried it with
something like `psihub`. But this means that every time I clone, I have to
change the url. This also messes with my editor, and sharing the url with
colleagues. I settled on writing a git-psi command that mimics clone, but sets
ssh options.

Copy the included git-psi shell command into your path, then run like:

	git psi git@github.com:psiservices/<repo>

If you forget and do a regular `git clone`, you can correct the setting at any time by running `git psi` by itself.
