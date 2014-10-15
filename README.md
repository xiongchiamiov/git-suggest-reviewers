Suggest code reviewers based on git history.

# Rationale

Code review is good, but deciding who should review your code is hard.  We have
a complete view of history performantly available in git, so we should be able
to use that to generate semi-reasonable suggestions.

# Installation

    [$]> curl -s https://raw.github.com/xiongchiamiov/git-suggest-reviewers/master/git-suggest-reviewers > ~/bin/git-suggest-reviewers
    [$]> chmod +x ~/bin/git-suggest-reviewers

# Usage

    Usage:
        git-suggest-reviewers [options] [<file>...]
    
    Options:
        -h --help     Show this screen.
        -v --version  Display program version.
    
    Arguments:
        <file>  A file whose history will be used to generate reviewers.  If none
                specified, all files will be used.

# Example

On [reddit/reddit](https://github.com/reddit/reddit):

    [$]> git suggest-reviewers
      45 Brian Simpson
      19 umbrae
      12 xiongchiamiov
       7 Neil Williams
       5 Jordan Milne
       4 Keith Mitchell
       3 Robert Ditthardt
       2 Chad Birch
       1 powerlanguage
       1 Jack Lawson
       1 Jack Kingsman
    [$]> git suggest-reviewers README.md
       3 Max Goodman
       1 Jason Harvey
    [$]> git suggest-reviewers README.md LICENSE
       3 Max Goodman
       2 Neil Williams
       1 spez
       1 Seth Woodworth
       1 KeyserSosa
       1 Jason Harvey
