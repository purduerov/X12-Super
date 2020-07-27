# X12-Super-Module

This is an advanced way to manage all the board repos for IEEE ROV. 
Each board's repo is treated as a submodule. 
Git submodules do not track the files inside a submodule, they only point to a commit in the submodule.

To get the version pointed at by the super module (this repo), run:
	`git submodule update --init --recursive`
	This can be accessed easier via:
		`git config --global alias.sup 'submodule update --init --recursive'`
		so that you can then type `git sup`
		
To get the latest version of each submodule, run:
	`git submodule foreach [--recursive] git pull`

To set up a new submodule, clone the repo with 
	`git clone link.copied.from.github`
	then do 
	`git submodule add X12-Boardname`
