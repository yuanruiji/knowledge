# knowledge

Bring branch info back to ubuntu's terminator cmd:

echo -e "parse_git_branch() {\n    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'\n}\nPS1=\"\$PS1\\\$(parse_git_branch)\"" >> ~/.bashrc; source ~/.bashrc
